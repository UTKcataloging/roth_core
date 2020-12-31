# OpenRefine Template for Roth Core

---

## Prefix

```
<?xml version="1.0" encoding="UTF-8"?>
<modsCollection xmlns="http://www.loc.gov/mods/v3" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xlink="http://www.w3.org/1999/xlink" xsi:schemaLocation="http://www.loc.gov/mods/v3 http://www.loc.gov/standards/mods/v3/mods-3-5.xsd">
```

## Row Template

```
<mods>
<identifier type="pid">{{cells["PID"].value}}</identifier>
<identifier type="local">{{cells["adminDB"].value}}</identifier>
<identifier>{{cells["DocumentID"].value}}</identifier>
<titleInfo><title>{{cells["title"].value}}</title></titleInfo>
{{if(isBlank(cells["abstract"].value),'', '<abstract>' + cells['abstract'].value + '</abstract>')}}
{{if(isBlank(cells["abstract2"].value),'', '<abstract>' + cells['abstract2'].value + '</abstract>')}}
<name authority="naf" valueURI="{{cells['creator_URI'].value}}">
<namePart>{{cells['creator'].value}}</namePart>
<role>
<roleTerm authority="marcrelator" valueURI="http://id.loc.gov/vocabulary/relators/pht">Photographer</roleTerm>
</role>
</name>
<originInfo>
{{if(isBlank(cells['dateCreated'].value), '', '<dateCreated>' + cells['dateCreated'].value + '</dateCreated>') + if(isBlank(cells['date_edtf'].value), '', '<dateCreated encoding="edtf">' + cells['date_edtf'].value + '</dateCreated>') + if(isBlank(cells['date_start'].value), '', '<dateCreated encoding="edtf" point="start">' + cells['date_start'].value + '</dateCreated><dateCreated encoding="edtf" point="end">' + cells['date_end'].value + '</dateCreated>') + if(isBlank(cells['circa'].value), '', '<dateCreated qualifier="approximate">' + cells['circa'].value + '</dateCreated><dateCreated qualifier="approximate" encoding="edtf">' + cells['date_approximate'].value + '</dateCreated>')}}
</originInfo>
<physicalDescription>
<form authority="aat" valueURI="http://vocab.getty.edu/aat/300046300">photographs</form>
<extent>4 inches x 6 inches</extent>
</physicalDescription>
{{if(isBlank(cells['subject2'].value), '', '<subject' + if(isBlank(cells['subject2_URI'].value), '', ' valueURI="' + cells['subject2_URI'].value + '"') + '><topic>' + cells['subject2'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject3'].value), '', '<subject' + if(isBlank(cells['subject3_URI'].value), '', ' valueURI="' + cells['subject3_URI'].value + '"') + '><topic>' + cells['subject3'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject4'].value), '', '<subject' + if(isBlank(cells['subject4_URI'].value), '', ' valueURI="' + cells['subject4_URI'].value + '"') + '><topic>' + cells['subject4'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject5'].value), '', '<subject' + if(isBlank(cells['subject5_URI'].value), '', ' valueURI="' + cells['subject5_URI'].value + '"') + '><topic>' + cells['subject5'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject6'].value), '', '<subject' + if(isBlank(cells['subject6_URI'].value), '', ' valueURI="' + cells['subject6_URI'].value + '"') + '><topic>' + cells['subject6'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject7'].value), '', '<subject' + if(isBlank(cells['subject7_URI'].value), '', ' valueURI="' + cells['subject7_URI'].value + '"') + '><topic>' + cells['subject7'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject8'].value), '', '<subject' + if(isBlank(cells['subject8_URI'].value), '', ' valueURI="' + cells['subject8_URI'].value + '"') + '><topic>' + cells['subject8'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject9'].value), '', '<subject' + if(isBlank(cells['subject9_URI'].value), '', ' valueURI="' + cells['subject9_URI'].value + '"') + '><topic>' + cells['subject9'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject10'].value), '', '<subject' + if(isBlank(cells['subject10_URI'].value), '', ' valueURI="' + cells['subject10_URI'].value + '"') + '><topic>' + cells['subject10'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject11'].value), '', '<subject' + if(isBlank(cells['subject11_URI'].value), '', ' valueURI="' + cells['subject11_URI'].value + '"') + '><topic>' + cells['subject11'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject12'].value), '', '<subject' + if(isBlank(cells['subject12_URI'].value), '', ' valueURI="' + cells['subject12_URI'].value + '"') + '><topic>' + cells['subject12'].value + '</topic></subject>')}}

{{if(isBlank(cells['subject_geographic'].value), '', '<subject' + if(isBlank(cells['subject_geographic_URI'].value), '', ' authority="' + cells['subject_geographic_auth'].value + '" valueURI="' + cells['subject_geographic_URI'].value + '"') + '><geographic>' + cells['subject_geographic'].value + '</geographic>' + if(isBlank(cells['coordinates'].value), '', '<cartographics><coordinates>' + cells['coordinates'].value + '</coordinates></cartographics>') + '</subject>')}}
{{if(isBlank(cells['subject_geo2'].value), '', '<subject' + if(isBlank(cells['subject_geo2_URI'].value), '', ' authority="' + cells['subject_geo2_auth'].value + '" valueURI="' + cells['subject_geo2_URI'].value + '"') + '><geographic>' + cells['subject_geo2'].value + '</geographic>' + if(isBlank(cells['coordinates2'].value), '', '<cartographics><coordinates>' + cells['coordinates2'].value + '</coordinates></cartographics>') + '</subject>')}}
{{if(isBlank(cells['subject_geo3'].value), '', '<subject' + if(isBlank(cells['subject_geo3_URI'].value), '', ' authority="' + cells['subject_geo3_auth'].value + '" valueURI="' + cells['subject_geo3_URI'].value + '"') + '><geographic>' + cells['subject_geo3'].value + '</geographic>' + if(isBlank(cells['coordinates3'].value), '', '<cartographics><coordinates>' + cells['coordinates3'].value + '</coordinates></cartographics>') + '</subject>')}}
{{if(isBlank(cells['subject_geo4'].value), '', '<subject' + if(isBlank(cells['subject_geo4_URI'].value), '', ' authority="' + cells['subject_geo4_auth'].value + '" valueURI="' + cells['subject_geo4_URI'].value + '"') + '><geographic>' + cells['subject_geo4'].value + '</geographic>' + if(isBlank(cells['coordinates4'].value), '', '<cartographics><coordinates>' + cells['coordinates4'].value + '</coordinates></cartographics>') + '</subject>')}}
{{if(isBlank(cells['subject_geo5'].value), '', '<subject' + if(isBlank(cells['subject_geo5_URI'].value), '', ' authority="' + cells['subject_geo5_auth'].value + '" valueURI="' + cells['subject_geo5_URI'].value + '"') + '><geographic>' + cells['subject_geo5'].value + '</geographic>' + if(isBlank(cells['coordinates5'].value), '', '<cartographics><coordinates>' + cells['coordinates5'].value + '</coordinates></cartographics>') + '</subject>')}}
{{if(isBlank(cells['subject_geo6'].value), '', '<subject' + if(isBlank(cells['subject_geo6_URI'].value), '', ' authority="' + cells['subject_geo6_auth'].value + '" valueURI="' + cells['subject_geo6_URI'].value + '"') + '><geographic>' + cells['subject_geo6'].value + '</geographic>' + if(isBlank(cells['coordinates6'].value), '', '<cartographics><coordinates>' + cells['coordinates6'].value + '</coordinates></cartographics>') + '</subject>')}}
{{if(isBlank(cells['subject_geo7'].value), '', '<subject authority="lcsh" valueURI="' + cells['subject_geo7_URI'].value + '"><geographic>' + cells['subject_geo7'].value + '</geographic></subject>')}}
{{if(isBlank(cells['subject_geo8'].value), '', '<subject' + if(isBlank(cells['subject_geo8_URI'].value), '', ' authority="' + cells['subject_geo8_auth'].value + '" valueURI="' + cells['subject_geo8_URI'].value + '"') + '><geographic>' + cells['subject_geo8'].value + '</geographic>' + if(isBlank(cells['coordinates8'].value), '', '<cartographics><coordinates>' + cells['coordinates8'].value + '</coordinates></cartographics>') + '</subject>')}}
{{if(isBlank(cells['subject_geo9'].value), '', '<subject' + if(isBlank(cells['subject_geo9_URI'].value), '', ' authority="' + cells['subject_geo9_auth'].value + '" valueURI="' + cells['subject_geo9_URI'].value + '"') + '><geographic>' + cells['subject_geo9'].value + '</geographic>' + if(isBlank(cells['coordinates9'].value), '', '<cartographics><coordinates>' + cells['coordinates9'].value + '</coordinates></cartographics>') + '</subject>')}}

{{if(isBlank(cells['subject_name'].value), '', '<subject' + if(isBlank(cells['subject_name_URI'].value), '', ' authority="naf" valueURI="' + cells['subject_name_URI'].value + '"') + '><name><namePart>' + cells['subject_name'].value + '</namePart></name></subject>')}}
{{if(isBlank(cells['subject_name2'].value), '', '<subject' + if(isBlank(cells['subject_name2_URI'].value), '', ' authority="naf" valueURI="' + cells['subject_name2_URI'].value + '"') + '><name><namePart>' + cells['subject_name2'].value + '</namePart></name></subject>')}}
{{if(isBlank(cells['subject_name3'].value), '', '<subject' + if(isBlank(cells['subject_name3_URI'].value), '', ' authority="naf" valueURI="' + cells['subject_name3_URI'].value + '"') + '><name><namePart>' + cells['subject_name3'].value + '</namePart></name></subject>')}}
{{if(isBlank(cells['subject_name4'].value), '', '<subject' + if(isBlank(cells['subject_name4_URI'].value), '', ' authority="naf" valueURI="' + cells['subject_name4_URI'].value + '"') + '><name><namePart>' + cells['subject_name4'].value + '</namePart></name></subject>')}}
{{if(isBlank(cells['subject_name5'].value), '', '<subject' + if(isBlank(cells['subject_name5_URI'].value), '', ' authority="naf" valueURI="' + cells['subject_name5_URI'].value + '"') + '><name><namePart>' + cells['subject_name5'].value + '</namePart></name></subject>')}}
{{if(isBlank(cells['subject_name6'].value), '', '<subject><name><namePart>' + cells['subject_name6'].value + '</namePart></name></subject>')}}
{{if(isBlank(cells['subject_name7'].value), '', '<subject' + if(isBlank(cells['subject_name7_URI'].value), '', ' authority="naf" valueURI="' + cells['subject_name7_URI'].value + '"') + '><name><namePart>' + cells['subject_name7'].value + '</namePart></name></subject>')}}
{{if(isBlank(cells['subject_name8'].value), '', '<subject' + if(isBlank(cells['subject_name8_URI'].value), '', ' authority="naf" valueURI="' + cells['subject_name8_URI'].value + '"') + '><name><namePart>' + cells['subject_name8'].value + '</namePart></name></subject>')}}

<typeOfResource>{{cells['typeOfResource'].value}}</typeOfResource>
<relatedItem displayLabel="Project" type="host"><titleInfo><title>Albert "Dutch" Roth Photograph Collection</title></titleInfo></relatedItem>
<relatedItem displayLabel="Collection" type="host"><titleInfo><title>A. G. "Dutch" and Margaret Ann Roth Papers</title></titleInfo><identifier>MS.3334</identifier></relatedItem>
<location><physicalLocation valueURI="http://id.loc.gov/authorities/names/no2014027633">University of Tennessee, Knoxville. Special Collections</physicalLocation></location>
<recordInfo><recordContentSource valueURI="http://id.loc.gov/authorities/names/n87808088">University of Tennessee, Knoxville. Libraries</recordContentSource></recordInfo>
<accessCondition type="use and reproduction" xlink:href="{{cells['rights_URI'].value}}">{{cells['rights'].value}}</accessCondition>
</mods>
```

## Row Separator

**LEAVE BLANK**

## Suffix

```
</modsCollection>
```