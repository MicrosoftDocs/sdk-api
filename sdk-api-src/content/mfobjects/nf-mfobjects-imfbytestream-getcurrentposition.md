---
UID: NF:mfobjects.IMFByteStream.GetCurrentPosition
title: IMFByteStream::GetCurrentPosition (mfobjects.h)
description: Retrieves the current read or write position in the stream.
old-location: mf\imfbytestream_getcurrentposition.htm
tech.root: medfound
ms.assetid: de36742a-a8a5-4f40-9fea-af89d9a6bf2e
ms.date: 12/05/2018
ms.keywords: GetCurrentPosition, GetCurrentPosition method [Media Foundation], GetCurrentPosition method [Media Foundation],IMFByteStream interface, IMFByteStream interface [Media Foundation],GetCurrentPosition method, IMFByteStream.GetCurrentPosition, IMFByteStream::GetCurrentPosition, de36742a-a8a5-4f40-9fea-af89d9a6bf2e, mf.imfbytestream_getcurrentposition, mfobjects/IMFByteStream::GetCurrentPosition
ms.topic: method
f1_keywords:
- mfobjects/IMFByteStream.GetCurrentPosition
dev_langs:
- c++
req.header: mfobjects.h
req.include-header: Mfidl.h
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
- IMFByteStream.GetCurrentPosition
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFByteStream::GetCurrentPosition


## -description


Retrieves the current read or write position in the stream.
        


## -parameters




### -param pqwPosition [out]

Receives the current position, in bytes.
          


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The methods that update the current position are <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-read">Read</a>, <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-beginread">BeginRead</a>, <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-write">Write</a>, <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-beginwrite">BeginWrite</a>, <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-setcurrentposition">SetCurrentPosition</a>, and <a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-seek">Seek</a>.
      

This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream">IMFByteStream</a>
 

 

