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

# IWMHeaderInfo2::GetCodecInfo


## -description



The <b>GetCodecInfo</b> method retrieves information about a codec that is used to create the content of a file.




## -parameters




### -param wIndex [in]

<b>DWORD</b>that contains the zero-based codec index.


### -param pcchName [in, out]

On input, pointer to the length of <i>pwszName</i> in wide characters. On output, pointer to a count of the characters that are used in <i>pwszName</i>.This includes the terminating <b>null</b> character.


### -param pwszName [out]

Pointer to a wide-character <b>null</b>-terminated string buffer into which the name of the codec is copied.


### -param pcchDescription [in, out]

On input, pointer to the length of <i>pwszDescription</i> in wide characters. On output, pointer to a count of the characters that are used in <i>pwszDescription</i>. This includes the terminating <b>null</b> character.


### -param pwszDescription [out]

Pointer to a wide-character <b>null</b>-terminated string buffer into which the description of the codec is copied.


### -param pCodecType [out]

Pointer to one member of the <a href="https://msdn.microsoft.com/31fcaa84-1b7e-407c-95dc-bf13263b788a">WMT_CODEC_INFO_TYPE</a> enumeration type.


### -param pcbCodecInfo [in, out]

On input, pointer to the length of <i>pbCodecInfo</i>, in bytes. On output, pointer to a count of the bytes used in <i>pbCodecInfo</i>.


### -param pbCodecInfo [out]

Pointer to a byte array.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.




## -remarks



You should make two calls to <b>GetCodecInfo</b>. On the first call, pass <b>NULL</b> for <i>pwszName</i>, <i>pwszDescription</i>, and <i>pbCodecInfo</i>. On return the values pointed to by <i>pcchName</i> and <i>pcchDescription</i> are set to the number of characters. These include the terminating <b>null</b> character, which is required to hold the name string in <i>pcchName</i> and the description string in <i>pcchDescription</i>. The value pointed to by <i>pcbCodecInfo</i> is set to the buffer size required to hold the codec information. With these sizes, you can allocate the required amount of memory to receive each value. Pass pointers to the buffers are <i>pwszName</i>, <i>pwszDescription</i>, and <i>pbCodecInfo</i> on the second call.

Use this method, and the <b>GetCodecInfoCount</b> method, to enumerate through the codec information.




## -see-also




<a href="https://msdn.microsoft.com/af670b54-f695-4b6f-8190-c25ea409b53a">IWMHeaderInfo2 Interface</a>



<a href="https://msdn.microsoft.com/1f77f362-5cc7-4d12-9b5f-0436d490b46d">IWMHeaderInfo2::GetCodecInfoCount</a>



<a href="https://msdn.microsoft.com/5791e330-3877-4d3a-b27f-f14b97d1a435">IWMHeaderInfo3</a>



<a href="https://msdn.microsoft.com/31fcaa84-1b7e-407c-95dc-bf13263b788a">WMT_CODEC_INFO_TYPE</a>
 

 

