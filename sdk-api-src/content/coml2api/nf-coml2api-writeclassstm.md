---
UID: NF:coml2api.WriteClassStm
title: WriteClassStm function
author: windows-sdk-content
description: The WriteClassStm function stores the specified CLSID in the stream.
old-location: stg\writeclassstm.htm
tech.root: Stg
ms.assetid: c08bfbc8-f7ac-4534-8c98-c732c6daa2f7
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: WriteClassStm, WriteClassStm function [Structured Storage], _stg_writeclassstm, coml2api/WriteClassStm, stg.writeclassstm
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: coml2api.h
req.include-header: Ole2.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ole32.dll
 - API-MS-Win-Core-Com-l2-1-1.dll
 - coml2.dll
api_name:
 - WriteClassStm
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WriteClassStm function


## -description


The <b>WriteClassStm</b> function stores the specified CLSID in the stream.


## -parameters




### -param pStm [in]


<a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a> pointer to the stream into which the CLSID is to be written.


### -param rclsid [in]

Specifies the CLSID to write to the stream.


## -returns



This function returns HRESULT.




## -remarks



The 
<b>WriteClassStm</b> function writes a CLSID to the specified stream object so it can be read by the 
<a href="https://msdn.microsoft.com/bcf11c5b-e164-4a0f-b30f-ee9e76c4356d">ReadClassStm</a> function. Most applications do not call 
<b>WriteClassStm</b> directly. OLE calls it before making a call to an object's 
<a href="_com_ipersiststream_save">IPersistStream::Save</a> method.




## -see-also




<a href="https://msdn.microsoft.com/90256fcd-54ce-48e1-aa12-d8f91cd4dfb1">ReadClassStg</a>



<a href="https://msdn.microsoft.com/bcf11c5b-e164-4a0f-b30f-ee9e76c4356d">ReadClassStm</a>



<a href="https://msdn.microsoft.com/5f2f16d1-923f-4ba7-8d4b-7e8535f6f15e">WriteClassStg</a>
 

 

