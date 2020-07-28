---
UID: NF:amvideo.IDirectDrawVideo.GetFourCCCodes
title: IDirectDrawVideo::GetFourCCCodes (amvideo.h)
description: The GetFourCCCodes method retrieves the multimedia format type.
helpviewer_keywords: ["GetFourCCCodes","GetFourCCCodes method [DirectShow]","GetFourCCCodes method [DirectShow]","IDirectDrawVideo interface","IDirectDrawVideo interface [DirectShow]","GetFourCCCodes method","IDirectDrawVideo.GetFourCCCodes","IDirectDrawVideo::GetFourCCCodes","IDirectDrawVideoGetFourCCCodes","amvideo/IDirectDrawVideo::GetFourCCCodes","dshow.idirectdrawvideo_getfourcccodes"]
old-location: dshow\idirectdrawvideo_getfourcccodes.htm
tech.root: dshow
ms.assetid: 3ea1c5c4-bf2e-40f6-bf48-a69900128ec8
ms.date: 12/05/2018
ms.keywords: GetFourCCCodes, GetFourCCCodes method [DirectShow], GetFourCCCodes method [DirectShow],IDirectDrawVideo interface, IDirectDrawVideo interface [DirectShow],GetFourCCCodes method, IDirectDrawVideo.GetFourCCCodes, IDirectDrawVideo::GetFourCCCodes, IDirectDrawVideoGetFourCCCodes, amvideo/IDirectDrawVideo::GetFourCCCodes, dshow.idirectdrawvideo_getfourcccodes
f1_keywords:
- amvideo/IDirectDrawVideo.GetFourCCCodes
dev_langs:
- c++
req.header: amvideo.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
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
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
api_name:
- IDirectDrawVideo.GetFourCCCodes
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDirectDrawVideo::GetFourCCCodes


## -description



The <code>GetFourCCCodes</code> method retrieves the multimedia format type.




## -parameters




### -param pCount

Pointer to the number of FOURCC codes in the <i>pCodes</i> array.


### -param pCodes

Pointer to an array of <b>DWORD</b> media tags formerly used for Microsoft multimedia types.


## -returns



Returns an <b>HRESULT</b> value.




## -remarks



In the original Windows multimedia APIs, media types were tagged with 32-bit values created from four 8-bit characters and were known as <i>FOURCC</i> codes. Because FOURCC codes are unique, a one-to-one mapping has been made possible by allocating a range of 4 billion GUIDs representing FOURCCs.

This method retrieves the FOURCC codes that the current display driver can support. The number available is obtained by calling the method with a valid <i>pCount</i> pointer, but with <i>pCodes</i> set to <b>NULL</b>. In this case, the <i>pCount</i> variable will be filled in with the number of FOURCC codes available. An application can then allocate enough <b>DWORD</b> values for this many FOURCC codes and call the method again with the array pointer in <i>pCodes</i>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/amvideo/nn-amvideo-idirectdrawvideo">IDirectDrawVideo Interface</a>
 

 

