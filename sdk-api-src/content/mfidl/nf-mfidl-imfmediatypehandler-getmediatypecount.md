---
UID: NF:mfidl.IMFMediaTypeHandler.GetMediaTypeCount
title: IMFMediaTypeHandler::GetMediaTypeCount
author: windows-sdk-content
description: Retrieves the number of media types in the object's list of supported media types.
old-location: mf\imfmediatypehandler_getmediatypecount.htm
tech.root: medfound
ms.assetid: c5ee41bc-ee8b-4990-ae9d-92ef54597f31
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: GetMediaTypeCount, GetMediaTypeCount method [Media Foundation], GetMediaTypeCount method [Media Foundation],IMFMediaTypeHandler interface, IMFMediaTypeHandler interface [Media Foundation],GetMediaTypeCount method, IMFMediaTypeHandler.GetMediaTypeCount, IMFMediaTypeHandler::GetMediaTypeCount, c5ee41bc-ee8b-4990-ae9d-92ef54597f31, mf.imfmediatypehandler_getmediatypecount, mfidl/IMFMediaTypeHandler::GetMediaTypeCount
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFMediaTypeHandler.GetMediaTypeCount
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFMediaTypeHandler::GetMediaTypeCount


## -description



Retrieves the number of media types in the object's list of supported media types.




## -parameters




### -param pdwTypeCount [out]

Receives the number of media types in the list.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



To get the supported media types, call <a href="https://msdn.microsoft.com/a1827675-bbc4-45d8-8c6e-644b0d2addd4">IMFMediaTypeHandler::GetMediaTypeByIndex</a>.
      

For a media source, the media type handler for each stream must contain at least one supported media type. For media sinks, the media type handler for each stream might contain zero media types. In that case, the application must provide the media type. To test whether a particular media type is supported, call <a href="https://msdn.microsoft.com/ea52defa-8b78-4f40-97ae-ed6a5ee4849e">IMFMediaTypeHandler::IsMediaTypeSupported</a>.
      

This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/5b937bf7-4f86-4dc1-a4d5-7e724dcf5b36">IMFMediaTypeHandler</a>
 

 

