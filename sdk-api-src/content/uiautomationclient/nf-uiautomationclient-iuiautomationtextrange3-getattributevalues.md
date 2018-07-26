---
UID: NF:uiautomationclient.IUIAutomationTextRange3.GetAttributeValues
title: IUIAutomationTextRange3::GetAttributeValues
author: windows-sdk-content
description: Returns all of the requested text attribute values for a text range in a single cross-process call. This is equivalent to calling GetAttributeValue, except it can retrieve multiple values instead of just one.
old-location: winauto\uiauto_IUIAutomationTextRange3_GetAttributeValues.htm
old-project: WinAuto
ms.assetid: 1AF29BF1-A074-4054-B338-7B6922B1415C
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: GetAttributeValues, GetAttributeValues method [Windows Accessibility], GetAttributeValues method [Windows Accessibility],IUIAutomationTextRange3 interface, IUIAutomationTextRange3 interface [Windows Accessibility],GetAttributeValues method, IUIAutomationTextRange3.GetAttributeValues, IUIAutomationTextRange3::GetAttributeValues, uiautomationclient/IUIAutomationTextRange3::GetAttributeValues, winauto.uiauto_IUIAutomationTextRange3_GetAttributeValues
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: uiautomationclient.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1703 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: UIAutomationClient.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: "*UI_ANIMATION_KEYFRAME"
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationClient.h
api_name:
 - IUIAutomationTextRange3.GetAttributeValues
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IUIAutomationTextRange3::GetAttributeValues


## -description


Returns all of the requested text attribute values for a text range in a single cross-process call.  This is equivalent to calling <a href="https://msdn.microsoft.com/7a77774e-7be0-473e-a0c9-e1aa108549e1">GetAttributeValue</a>, except it can retrieve multiple values instead of just one.


## -parameters




### -param attributeIds [in]

A list of <a href="https://msdn.microsoft.com/67d86817-6a3f-4047-88d9-34f33f52a563">text attribute identifiers</a>.


### -param attributeIdCount [in]

The number of <a href="https://msdn.microsoft.com/67d86817-6a3f-4047-88d9-34f33f52a563">text attribute identifiers</a> in the <i>attributeIds</i> list.


### -param attributeValues [out, retval]

A <b>SAFEARRAY</b> of <b>VARIANT</b> containing values to corresponding text attributes for a text range.


## -returns



Returns <b>S_OK</b> if successful, otherwise an <b>HRESULT</b> error code.




## -remarks



<b>GetAttributeValues</b> only gets the text attributes that are supplied in the call.




## -see-also




<a href="https://msdn.microsoft.com/3491996E-89EF-496D-94B6-FF8D121D3828">IUIAutomationTextRange3</a>



<a href="https://msdn.microsoft.com/98a82ff8-f4b9-4f62-ae69-31a2c18de70e">UI Automation Support for Textual Content</a>
 

 

