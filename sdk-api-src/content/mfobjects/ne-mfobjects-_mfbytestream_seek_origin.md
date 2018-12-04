---
UID: NE:mfobjects._MFBYTESTREAM_SEEK_ORIGIN
title: "_MFBYTESTREAM_SEEK_ORIGIN"
author: windows-sdk-content
description: Specifies the origin for a seek request.
old-location: mf\mfbytestream_seek_origin.htm
tech.root: medfound
ms.assetid: ad7ad61a-0c02-4a8f-96c3-33f7d1f0ce51
ms.author: windowssdkdev
ms.date: 11/23/2018
ms.keywords: MFBYTESTREAM_SEEK_ORIGIN, MFBYTESTREAM_SEEK_ORIGIN enumeration [Media Foundation], _MFBYTESTREAM_SEEK_ORIGIN, ad7ad61a-0c02-4a8f-96c3-33f7d1f0ce51, mf.mfbytestream_seek_origin, mfobjects/MFBYTESTREAM_SEEK_ORIGIN, mfobjects/msoBegin, mfobjects/msoCurrent, msoBegin, msoCurrent
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mfobjects.h
api_name:
 - MFBYTESTREAM_SEEK_ORIGIN
product: Windows
targetos: Windows
req.typenames: MFBYTESTREAM_SEEK_ORIGIN
req.redist: 
---

# _MFBYTESTREAM_SEEK_ORIGIN enumeration


## -description



Specifies the origin for a seek request.




## -enum-fields




### -field msoBegin

The seek position is specified relative to the start of the stream.


### -field msoCurrent

The seek position is specified relative to the current read/write position in the stream.


## -see-also




<a href="https://msdn.microsoft.com/512c67a5-e87d-4a81-8577-e64dac868c40">IMFByteStream::Seek</a>



<a href="https://msdn.microsoft.com/f26a730f-18c4-4247-acaf-af1dfad19086">Media Foundation Enumerations</a>
 

 

