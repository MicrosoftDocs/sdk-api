---
UID: NF:uiautomationclient.IUIAutomationElement7.GetCurrentMetadataValue
title: IUIAutomationElement7::GetCurrentMetadataValue (uiautomationclient.h)
description: Gets metadata from the UI Automation element that indicates how the information should be interpreted.
old-location: winauto\uiauto_IUIAutomationElement7_GetCurrentMetadataValue.htm
tech.root: WinAuto
ms.assetid: 09FAECD6-2BD9-4C35-8798-5FF6311CC672
ms.date: 12/05/2018
ms.keywords: GetCurrentMetadataValue, GetCurrentMetadataValue method [Windows Accessibility], GetCurrentMetadataValue method [Windows Accessibility],IUIAutomationElement7 interface, IUIAutomationElement7 interface [Windows Accessibility],GetCurrentMetadataValue method, IUIAutomationElement7.GetCurrentMetadataValue, IUIAutomationElement7::GetCurrentMetadataValue, uiautomationclient/IUIAutomationElement7::GetCurrentMetadataValue, winauto.uiauto_IUIAutomationElement7_GetCurrentMetadataValue
ms.topic: method
f1_keywords:
- uiautomationclient/IUIAutomationElement7.GetCurrentMetadataValue
dev_langs:
- c++
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
- IUIAutomationElement7.GetCurrentMetadataValue
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUIAutomationElement7::GetCurrentMetadataValue


## -description


Gets metadata from the UI Automation element that indicates how the information should be interpreted. For example, should the string "1/4" be interpreted as a fraction or a date?


## -parameters




### -param targetId [in]

The ID of the property to retrieve.


### -param metadataId [in]

Specifies the type of metadata to retrieve.


### -param returnVal [out, retval]

The metadata.


## -returns



Returns <b>S_OK</b> if successful, otherwise an <b>HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationelement7">IUIAutomationElement7</a>



<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/ne-uiautomationcore-sayasinterpretas">SayAsInterpretAs</a>
 

 

