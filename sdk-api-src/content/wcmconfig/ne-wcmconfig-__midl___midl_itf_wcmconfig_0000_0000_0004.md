---
UID: NE:wcmconfig.__MIDL___MIDL_itf_wcmconfig_0000_0000_0004
title: "__MIDL___MIDL_itf_wcmconfig_0000_0000_0004"
author: windows-sdk-content
description: Describes setting types that are returned from the ISettingsItem::GetSettingType method and defines the object model type for the calling ISettingsItem interface.
old-location: smi\wcmsettingtype.htm
old-project: smi
ms.assetid: e7dbe536-778a-445c-929b-56e490fdeffb
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: WcmSettingType, WcmSettingType enumeration [SMI], __MIDL___MIDL_itf_wcmconfig_0000_0000_0004, settingTypeComplex, settingTypeList, settingTypeScalar, smi.wcmsettingtype, wcmconfig/WcmSettingType, wcmconfig/settingTypeComplex, wcmconfig/settingTypeList, wcmconfig/settingTypeScalar
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
tech.root: 
req.typenames: WcmSettingType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WcmConfig.h
api_name:
 - WcmSettingType
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# __MIDL___MIDL_itf_wcmconfig_0000_0000_0004 enumeration


## -description


Describes setting types that are returned from the <a href="https://msdn.microsoft.com/d222939f-9295-4751-8b32-586fa9930177">ISettingsItem::GetSettingType</a> method  and defines the object model type for the calling <a href="https://msdn.microsoft.com/a743d942-69f9-426b-be88-adf88b9bb1e0">ISettingsItem</a> interface.


## -enum-fields




### -field settingTypeScalar

For items of this type, you can call the <a href="https://msdn.microsoft.com/6ccb99aa-35d5-4f0b-a4f3-a42c4579bc4a">ISettingsItem::GetDataType</a>, <a href="https://msdn.microsoft.com/11b61570-d1ed-4dcf-b533-873096ae80b9">ISettingsItem::GetValue</a>, <a href="https://msdn.microsoft.com/2b4b96df-1286-49be-869a-404adaead27a">ISettingsItem::GetValueRaw</a>, <a href="https://msdn.microsoft.com/14bc4956-e8ea-464b-949e-ddc7ae445c1a">ISettingsItem::GetRestriction</a>, <a href="https://msdn.microsoft.com/64cf82d5-c210-4ff2-a7c8-1a284859382e">ISettingsItem::GetRestrictionFacets</a>, <a href="https://msdn.microsoft.com/52b7e852-b389-47ec-a9d0-e4ce2e95f1f8">ISettingsItem::SetValue</a>, and <a href="https://msdn.microsoft.com/65925c16-7a12-440f-ba2d-9156e41049ba">ISettingsItem::SetValueRaw</a> methods.


### -field settingTypeComplex

Items of this type may have children. You may call the <a href="https://msdn.microsoft.com/33bd7f91-c414-420e-bc18-1114924b93e9">ISettingsItem::Children</a>, <a href="https://msdn.microsoft.com/4a3d3212-bd47-46fb-9ce1-79ac109c6444">ISettingsItem::GetChild</a>, or <a href="https://msdn.microsoft.com/6c22cb66-5116-4107-9fb0-a6a4161b6f8e">ISettingsItem::HasChild</a> methods on this setting type.


### -field settingTypeList

Items of this type may have children. You may call the <a href="https://msdn.microsoft.com/33bd7f91-c414-420e-bc18-1114924b93e9">ISettingsItem::Children</a>, <a href="https://msdn.microsoft.com/4a3d3212-bd47-46fb-9ce1-79ac109c6444">ISettingsItem::GetChild</a>, or <a href="https://msdn.microsoft.com/6c22cb66-5116-4107-9fb0-a6a4161b6f8e">ISettingsItem::HasChild</a> methods on this setting type. You can also call the <a href="https://msdn.microsoft.com/c18fd849-aaa5-49d0-9e72-b3134a6f2be8">ISettingsItem::CreateListElement</a> and <a href="https://msdn.microsoft.com/4dca22b5-b4e3-4bb6-9eb4-5507472b63b2">ISettingsItem::RemoveListElement</a> methods  on children of items of this type.


## -remarks



<div class="alert"><b>Note</b>  All methods of the <a href="https://msdn.microsoft.com/a743d942-69f9-426b-be88-adf88b9bb1e0">ISettingsItem</a> interface, other than the ones that are explicitly described for a particular type, may be called on any type of setting.</div>
<div> </div>


