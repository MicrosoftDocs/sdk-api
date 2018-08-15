---
UID: NF:wmsdkidl.IWMReaderCallbackAdvanced.OnOutputPropsChanged
title: IWMReaderCallbackAdvanced::OnOutputPropsChanged
author: windows-sdk-content
description: The OnOutputPropsChanged method indicates that the media properties for the specified output have changed. This change occurs as a result of a call to the IWMReader::SetOutputProps method.
old-location: wmformat\iwmreadercallbackadvanced_onoutputpropschanged.htm
old-project: wmformat
ms.assetid: 5e8193c4-5fc7-4b19-9f6e-6873ebe5156a
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IWMReaderCallbackAdvanced interface [windows Media Format],OnOutputPropsChanged method, IWMReaderCallbackAdvanced.OnOutputPropsChanged, IWMReaderCallbackAdvanced::OnOutputPropsChanged, IWMReaderCallbackAdvancedOnOutputPropsChanged, OnOutputPropsChanged, OnOutputPropsChanged method [windows Media Format], OnOutputPropsChanged method [windows Media Format],IWMReaderCallbackAdvanced interface, wmformat.iwmreadercallbackadvanced_onoutputpropschanged, wmsdkidl/IWMReaderCallbackAdvanced::OnOutputPropsChanged
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 7 SDK, or later versions of the SDK
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WM_AETYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wmsdkidl.h
api_name:
 - IWMReaderCallbackAdvanced.OnOutputPropsChanged
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
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



To use this method, you must implement it in your application. You can return whatever <b>HRESULT</b> error codes are appropriate to your implementation. For more information about the <b>HRESULT</b> error codes included for use by the Windows Media Format SDK, see <a href="https://msdn.microsoft.com/ea1c129b-c0d7-4a1b-934c-c1c07364d4a8">Error Codes</a>.




## -remarks



This method is called by the reader if the caller gets an asynchronous result from the <b>SetOutputProps</b> method call. The next sample received for this output has these properties. After a call to <b>SetOutputProps</b> and before <b>OnOutputPropsChanged</b> is called, the contents of the media type are undefined.




## -see-also




<a href="https://msdn.microsoft.com/9d18961a-5ea4-4f3e-b473-7399e155f800">IWMReaderCallbackAdvanced Interface</a>
 

 

