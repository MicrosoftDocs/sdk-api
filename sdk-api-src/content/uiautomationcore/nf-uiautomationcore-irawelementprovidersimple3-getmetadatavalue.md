---
UID: NF:uiautomationcore.IRawElementProviderSimple3.GetMetadataValue
title: IRawElementProviderSimple3::GetMetadataValue
author: windows-sdk-content
description: Gets metadata from the UI Automation element that indicates how the information should be interpreted.
old-location: winauto\uiauto_IRawElementProviderSimple3_GetMetadataValue.htm
tech.root: WinAuto
ms.assetid: 832154F3-22D3-48E9-BC4E-CB495BB72485
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: GetMetadataValue, GetMetadataValue method [Windows Accessibility], GetMetadataValue method [Windows Accessibility],IRawElementProviderSimple3 interface, IRawElementProviderSimple3 interface [Windows Accessibility],GetMetadataValue method, IRawElementProviderSimple3.GetMetadataValue, IRawElementProviderSimple3::GetMetadataValue, uiautomationcore/IRawElementProviderSimple3::GetMetadataValue, winauto.uiauto_IRawElementProviderSimple3_GetMetadataValue
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: uiautomationcore.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1703 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: UIAutomationCore.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: UIAutomationCore.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationCore.dll
api_name:
 - IRawElementProviderSimple3.GetMetadataValue
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- uiautomationcore.h
: 
- IRawElementProviderSimple3.GetMetadataValue
: 
---

# IRawElementProviderSimple3::GetMetadataValue


## -description


Gets metadata from the UI Automation element that indicates how the information should be interpreted. For example, should the string "1/4" be interpreted as a fraction or a date?


## -parameters




### -param targetId [in]

The ID of the property to retrieve.


### -param metadataId [in]

Specifies the type of metadata to retrieve.


### -param returnVal

TBD




#### - pRetVal [out, retval]

The metadata.


## -returns



Returns <b>S_OK</b> if successful, otherwise an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Mt798231(v=VS.85).aspx">IRawElementProviderSimple3</a>



<a href="https://msdn.microsoft.com/70F6AA0E-52CB-49D4-BBAF-2B6367D5E44D">SayAsInterpretAs</a>
 

 

