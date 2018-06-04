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

# IWMReaderCallbackAdvanced::OnStreamSelection


## -description



The <b>OnStreamSelection</b> method notifies the application of stream changes made due to bandwidth restrictions. To have this method called, call <a href="https://msdn.microsoft.com/8cb0bd59-2a46-4cdc-9a88-ee6a8f170f3c">IWMReaderAdvanced::SetReceiveSelectionCallbacks</a>.




## -parameters




### -param wStreamCount [in]

<b>WORD</b> containing the number of entries in the <i>pStreamNumbers</i> array.


### -param pStreamNumbers [in]

Pointer to an array of stream numbers.


### -param pSelections [in]

Pointer to an array of members of the <a href="https://msdn.microsoft.com/7191d608-1a25-48c0-858b-c5e93f9d8e6e">WMT_STREAM_SELECTION</a> enumeration type. Each element in this array corresponds to the stream number contained in the corresponding element of the array pointed to by <i>pStreamNumbers</i>.


### -param pvContext [in]

Generic pointer, for use by the application. This pointer is the context pointer given to the <a href="https://msdn.microsoft.com/485844c6-7a84-4a0d-827d-060d8caef6cc">IWMReader::Start</a> method.


## -returns



To use this method, you must implement it in your application. You can return whatever <b>HRESULT</b> error codes are appropriate to your implementation. For more information about the <b>HRESULT</b> error codes included for use by the Windows Media Format SDK, see <a href="https://msdn.microsoft.com/library/windows/hardware/dn938542">Error Codes</a>.




## -remarks



Stream numbers are in the range of 1 through 63.

The application can also get callbacks when stream changes due to bandwidth restrictions occur.




## -see-also




<a href="https://msdn.microsoft.com/9d18961a-5ea4-4f3e-b473-7399e155f800">IWMReaderCallbackAdvanced Interface</a>
 

 

