---
UID: NF:mfobjects.IMFByteStream.GetLength
title: IMFByteStream::GetLength
author: windows-driver-content
description: Retrieves the length of the stream.
old-location: mf\imfbytestream_getlength.htm
old-project: medfound
ms.assetid: 6fb817a6-5b43-4716-a997-bbd8a0b9305d
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: 6fb817a6-5b43-4716-a997-bbd8a0b9305d, GetLength, GetLength method [Media Foundation], GetLength method [Media Foundation],IMFByteStream interface, IMFByteStream interface [Media Foundation],GetLength method, IMFByteStream.GetLength, IMFByteStream::GetLength, mf.imfbytestream_getlength, mfobjects/IMFByteStream::GetLength
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfobjects.h
req.include-header: Mfidl.h
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
req.typenames: MF_FILE_FLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfuuid.lib
-	mfuuid.dll
api_name:
-	IMFByteStream.GetLength
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFByteStream::GetLength


## -description



          Retrieves the length of the stream.
        


## -parameters




### -param pqwLength [out]


            Receives the length of the stream, in bytes. If the length is unknown, this value is -1.
          


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/690035b7-2855-4714-938f-f8250ec70d24">IMFByteStream</a>
 

 

