---
UID: NF:coml2api.WriteClassStg
title: WriteClassStg function
author: windows-sdk-content
description: The WriteClassStg function stores the specified class identifier (CLSID) in a storage object.
old-location: stg\writeclassstg.htm
old-project: stg
ms.assetid: 5f2f16d1-923f-4ba7-8d4b-7e8535f6f15e
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: WriteClassStg, WriteClassStg function [Structured Storage], _stg_writeclassstg, coml2api/WriteClassStg, stg.writeclassstg
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: CATEGORYINFO, *LPCATEGORYINFO
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
 - WriteClassStg
product: Windows
targetos: Windows
req.lib: Ole32.lib
req.dll: Ole32.dll
req.irql: 
---

# WriteClassStg function


## -description


The <b>WriteClassStg</b> function stores the specified class identifier (CLSID) in a storage object.


## -parameters




### -param pStg [in]


<a href="https://msdn.microsoft.com/2f454538-0f40-4811-b908-cd317ef79487">IStorage</a> pointer to the storage object that gets a new CLSID.


### -param rclsid [in]

Pointer to the CLSID to be stored with the object.


## -returns



This function returns HRESULT.




## -remarks



The 
<b>WriteClassStg</b> function writes a CLSID to the specified storage object so that it can be read by the 
<a href="https://msdn.microsoft.com/90256fcd-54ce-48e1-aa12-d8f91cd4dfb1">ReadClassStg</a> function. Container applications typically call this function before calling the 
<a href="https://msdn.microsoft.com/en-us/library/ms680680(v=VS.85).aspx">IPersistStorage::Save</a> method.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms691490(v=VS.85).aspx">OleSave</a>



<a href="https://msdn.microsoft.com/90256fcd-54ce-48e1-aa12-d8f91cd4dfb1">ReadClassStg</a>
 

 

