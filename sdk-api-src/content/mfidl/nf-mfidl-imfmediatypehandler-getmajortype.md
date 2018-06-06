---
UID: NF:mfidl.IMFMediaTypeHandler.GetMajorType
title: IMFMediaTypeHandler::GetMajorType
author: windows-sdk-content
description: Gets the major media type of the object.
old-location: mf\imfmediatypehandler_getmajortype.htm
old-project: medfound
ms.assetid: 1560d113-80a9-48bb-9f3d-6e3a288db962
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: 1560d113-80a9-48bb-9f3d-6e3a288db962, GetMajorType, GetMajorType method [Media Foundation], GetMajorType method [Media Foundation],IMFMediaTypeHandler interface, IMFMediaTypeHandler interface [Media Foundation],GetMajorType method, IMFMediaTypeHandler.GetMajorType, IMFMediaTypeHandler::GetMajorType, mf.imfmediatypehandler_getmajortype, mfidl/IMFMediaTypeHandler::GetMajorType
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps | UWP apps]
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
req.typenames: MFSensorDeviceMode
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFMediaTypeHandler.GetMajorType
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFMediaTypeHandler::GetMajorType


## -description


Gets the major media type of the object.
        


## -parameters




### -param pguidMajorType [out]

Receives a GUID that identifies the major type. For a list of possible values, see <a href="https://msdn.microsoft.com/1cca3539-a920-4938-93b9-ae41e1c0a287">Major Media Types</a>.
          


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The major type identifies what kind of data is in the stream, such as audio or video. To get the specific details of the format, call <a href="https://msdn.microsoft.com/b1676e40-81a2-4311-bba6-528bfa45a708">IMFMediaTypeHandler::GetCurrentMediaType</a>.

This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/5b937bf7-4f86-4dc1-a4d5-7e724dcf5b36">IMFMediaTypeHandler</a>
 

 

