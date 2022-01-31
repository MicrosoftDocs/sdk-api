---
UID: NE:wcmconfig.__MIDL___MIDL_itf_wcmconfig_0000_0000_0004
title: WcmSettingType (wcmconfig.h)
description: Describes setting types that are returned from the ISettingsItem::GetSettingType method and defines the object model type for the calling ISettingsItem interface.
helpviewer_keywords: ["WcmSettingType","WcmSettingType enumeration [SMI]","settingTypeComplex","settingTypeList","settingTypeScalar","smi.wcmsettingtype","wcmconfig/WcmSettingType","wcmconfig/settingTypeComplex","wcmconfig/settingTypeList","wcmconfig/settingTypeScalar"]
old-location: smi\wcmsettingtype.htm
tech.root: SMI
ms.assetid: e7dbe536-778a-445c-929b-56e490fdeffb
ms.date: 12/05/2018
ms.keywords: WcmSettingType, WcmSettingType enumeration [SMI], settingTypeComplex, settingTypeList, settingTypeScalar, smi.wcmsettingtype, wcmconfig/WcmSettingType, wcmconfig/settingTypeComplex, wcmconfig/settingTypeList, wcmconfig/settingTypeScalar
req.header: wcmconfig.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WcmConfig.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: WcmSettingType
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_wcmconfig_0000_0000_0004
 - wcmconfig/__MIDL___MIDL_itf_wcmconfig_0000_0000_0004
 - WcmSettingType
 - wcmconfig/WcmSettingType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WcmConfig.h
api_name:
 - WcmSettingType
---

# WcmSettingType enumeration


## -description

Describes setting types that are returned from the <a href="/previous-versions/windows/desktop/api/wcmconfig/nf-wcmconfig-isettingsitem-getsettingtype">ISettingsItem::GetSettingType</a> method  and defines the object model type for the calling <a href="/previous-versions/windows/desktop/api/wcmconfig/nn-wcmconfig-isettingsitem">ISettingsItem</a> interface.

## -enum-fields

### -field settingTypeScalar:1

For items of this type, you can call the <a href="/previous-versions/windows/desktop/api/wcmconfig/nf-wcmconfig-isettingsitem-getdatatype">ISettingsItem::GetDataType</a>, <a href="/previous-versions/windows/desktop/api/wcmconfig/nf-wcmconfig-isettingsitem-getvalue">ISettingsItem::GetValue</a>, <a href="/previous-versions/windows/desktop/api/wcmconfig/nf-wcmconfig-isettingsitem-getvalueraw">ISettingsItem::GetValueRaw</a>, <a href="/previous-versions/windows/desktop/api/wcmconfig/nf-wcmconfig-isettingsitem-getrestriction">ISettingsItem::GetRestriction</a>, <a href="/previous-versions/windows/desktop/api/wcmconfig/nf-wcmconfig-isettingsitem-getrestrictionfacets">ISettingsItem::GetRestrictionFacets</a>, <a href="/previous-versions/windows/desktop/api/wcmconfig/nf-wcmconfig-isettingsitem-setvalue">ISettingsItem::SetValue</a>, and <a href="/previous-versions/windows/desktop/api/wcmconfig/nf-wcmconfig-isettingsitem-setvalueraw">ISettingsItem::SetValueRaw</a> methods.

### -field settingTypeComplex:2

Items of this type may have children. You may call the <a href="/previous-versions/windows/desktop/api/wcmconfig/nf-wcmconfig-isettingsitem-children">ISettingsItem::Children</a>, <a href="/previous-versions/windows/desktop/api/wcmconfig/nf-wcmconfig-isettingsitem-getchild">ISettingsItem::GetChild</a>, or <a href="/previous-versions/windows/desktop/api/wcmconfig/nf-wcmconfig-isettingsitem-haschild">ISettingsItem::HasChild</a> methods on this setting type.

### -field settingTypeList:3

Items of this type may have children. You may call the <a href="/previous-versions/windows/desktop/api/wcmconfig/nf-wcmconfig-isettingsitem-children">ISettingsItem::Children</a>, <a href="/previous-versions/windows/desktop/api/wcmconfig/nf-wcmconfig-isettingsitem-getchild">ISettingsItem::GetChild</a>, or <a href="/previous-versions/windows/desktop/api/wcmconfig/nf-wcmconfig-isettingsitem-haschild">ISettingsItem::HasChild</a> methods on this setting type. You can also call the <a href="/previous-versions/windows/desktop/api/wcmconfig/nf-wcmconfig-isettingsitem-createlistelement">ISettingsItem::CreateListElement</a> and <a href="/previous-versions/windows/desktop/api/wcmconfig/nf-wcmconfig-isettingsitem-removelistelement">ISettingsItem::RemoveListElement</a> methods  on children of items of this type.

## -remarks

<div class="alert"><b>Note</b>  All methods of the <a href="/previous-versions/windows/desktop/api/wcmconfig/nn-wcmconfig-isettingsitem">ISettingsItem</a> interface, other than the ones that are explicitly described for a particular type, may be called on any type of setting.</div>
<div> </div>
