---
UID: NF:coml2api.ReadClassStm
title: ReadClassStm function
author: windows-sdk-content
description: Reads the CLSID previously written to a stream object with the WriteClassStm function.
old-location: stg\readclassstm.htm
old-project: Stg
ms.assetid: bcf11c5b-e164-4a0f-b30f-ee9e76c4356d
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: ReadClassStm, ReadClassStm function [Structured Storage], _stg_readclassstm, coml2api/ReadClassStm, stg.readclassstm
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: coml2api.h
req.include-header: Ole2.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
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
req.typenames: CATEGORYINFO, *LPCATEGORYINFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Ole32.dll
-	API-MS-Win-Core-Com-l2-1-1.dll
-	coml2.dll
api_name:
-	ReadClassStm
product: Windows
targetos: Windows
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
---

# ReadClassStm function


## -description


The 
<b>ReadClassStm</b> function
			reads the CLSID previously written to a stream object with the 
<a href="https://msdn.microsoft.com/c08bfbc8-f7ac-4534-8c98-c732c6daa2f7">WriteClassStm</a> function.


## -parameters




### -param pStm [in]

A pointer to the 
<a href="https://msdn.microsoft.com/c6f60e37-eadc-46a1-94f6-cacc23613531">IStream</a> interface on the stream object that contains the CLSID to be read. This CLSID must have been previously written to the stream object using 
<a href="https://msdn.microsoft.com/c08bfbc8-f7ac-4534-8c98-c732c6daa2f7">WriteClassStm</a>.


### -param pclsid [out]

A pointer to where the CLSID is to be written.


## -returns



This function also returns any of the error values returned by the 
<a href="https://msdn.microsoft.com/934a90bb-5ed0-4d80-9906-352ad8586655">ISequentialStream::Read</a> method.




## -remarks



Most applications do not call the 
<b>ReadClassStm</b> function directly. COM calls it before making a call to an object's 
<a href="_com_ipersiststream_load">IPersistStream::Load</a> implementation.




## -see-also




<a href="https://msdn.microsoft.com/90256fcd-54ce-48e1-aa12-d8f91cd4dfb1">ReadClassStg</a>



<a href="https://msdn.microsoft.com/5f2f16d1-923f-4ba7-8d4b-7e8535f6f15e">WriteClassStg</a>



<a href="https://msdn.microsoft.com/c08bfbc8-f7ac-4534-8c98-c732c6daa2f7">WriteClassStm</a>
 

 

