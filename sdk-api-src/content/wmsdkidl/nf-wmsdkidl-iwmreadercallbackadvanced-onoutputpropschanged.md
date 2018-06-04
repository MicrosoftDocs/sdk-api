---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IWMReaderCallbackAdvanced::OnOutputPropsChanged


## -description



The <b>OnOutputPropsChanged</b> method indicates that the media properties for the specified output have changed. This change occurs as a result of a call to the <a href="https://msdn.microsoft.com/0a5325d1-880b-4d65-96af-9d311dca989b">IWMReader::SetOutputProps</a> method.




## -parameters




### -param dwOutputNum [in]

<b>DWORD</b> containing the output number.


### -param pMediaType [in]

Pointer to a <a href="https://msdn.microsoft.com/37a9ac59-e152-47e1-96ee-b816cd645936">WM_MEDIA_TYPE</a> structure.


### -param pvContext [in]

Generic pointer, for use by the application. This pointer is the context pointer given to the <b>IWMReader::Start</b> method.


## -returns



To use this method, you must implement it in your application. You can return whatever <b>HRESULT</b> error codes are appropriate to your implementation. For more information about the <b>HRESULT</b> error codes included for use by the Windows Media Format SDK, see <a href="https://msdn.microsoft.com/library/windows/hardware/dn938542">Error Codes</a>.




## -remarks



This method is called by the reader if the caller gets an asynchronous result from the <b>SetOutputProps</b> method call. The next sample received for this output has these properties. After a call to <b>SetOutputProps</b> and before <b>OnOutputPropsChanged</b> is called, the contents of the media type are undefined.




## -see-also




<a href="https://msdn.microsoft.com/9d18961a-5ea4-4f3e-b473-7399e155f800">IWMReaderCallbackAdvanced Interface</a>
 

 

