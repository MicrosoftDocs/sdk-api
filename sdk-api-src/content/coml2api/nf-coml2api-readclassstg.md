---
UID: NF:coml2api.ReadClassStg
title: ReadClassStg function
author: windows-sdk-content
description: The ReadClassStg function reads the CLSID previously written to a storage object with the WriteClassStg function.
old-location: stg\readclassstg.htm
tech.root: Stg
ms.assetid: 90256fcd-54ce-48e1-aa12-d8f91cd4dfb1
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: ReadClassStg, ReadClassStg function [Structured Storage], _stg_readclassstg, coml2api/ReadClassStg, stg.readclassstg
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
 - ReadClassStg
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- ReadClassStg
: 
---

# ReadClassStg function


## -description


The <b>ReadClassStg</b> function
			reads the CLSID previously written to a storage object with the 
<a href="https://msdn.microsoft.com/en-us/library/Aa380384(v=VS.85).aspx">WriteClassStg</a> function.


## -parameters




### -param pStg [in]

Pointer to the 
<a href="https://msdn.microsoft.com/en-us/library/Aa380015(v=VS.85).aspx">IStorage</a> interface on the storage object containing the CLSID to be retrieved.


### -param pclsid [out]

Pointer to where the CLSID is written. May return CLSID_NULL.


## -returns



This function supports the standard return value E_OUTOFMEMORY, in addition to the following:

This function also returns any of the error values returned by the 
<a href="https://msdn.microsoft.com/en-us/library/Aa380033(v=VS.85).aspx">IStorage::Stat</a> method.




## -remarks



<b>ReadClassStg</b> is a helper function that calls the <a href="https://msdn.microsoft.com/en-us/library/Aa380033(v=VS.85).aspx">IStorage::Stat</a> method and retrieves the CLSID previously written to the storage object with a call to 
<a href="https://msdn.microsoft.com/en-us/library/Aa380384(v=VS.85).aspx">WriteClassStg</a> from the 
<a href="https://msdn.microsoft.com/en-us/library/Aa380319(v=VS.85).aspx">STATSTG</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa380033(v=VS.85).aspx">IStorage::Stat</a>



<a href="https://msdn.microsoft.com/en-us/library/ms694338(v=VS.85).aspx">OleLoad</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa380319(v=VS.85).aspx">STATSTG</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa380384(v=VS.85).aspx">WriteClassStg</a>
 

 

