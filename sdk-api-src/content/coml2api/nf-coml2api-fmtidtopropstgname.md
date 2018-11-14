---
UID: NF:coml2api.FmtIdToPropStgName
title: FmtIdToPropStgName function
author: windows-sdk-content
description: Converts a property set format identifier (FMTID) to its storage or stream name.
old-location: stg\fmtidtopropstgname.htm
tech.root: Stg
ms.assetid: 044f8883-bbd2-4cd3-b9dc-739ecb711bdd
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: FmtIdToPropStgName, FmtIdToPropStgName function [Structured Storage], _stg_fmtidtopropstgname, coml2api/FmtIdToPropStgName, stg.fmtidtopropstgname
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: coml2api.h
req.include-header: Propidl.h
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
 - FmtIdToPropStgName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- FmtIdToPropStgName
: 
---

# FmtIdToPropStgName function


## -description


The <b>FmtIdToPropStgName</b> function converts a property set format identifier (FMTID) to its storage or stream name.


## -parameters




### -param pfmtid [in]

A pointer to the FMTID of the property set.


### -param oszName [out]

A pointer to a null-terminated string that receives the storage or stream name of the property set identified by <i>pfmtid</i>. The array allocated for this string must be at least CCH_MAX_PROPSTG_NAME (32) characters in length.


## -returns



This function supports the standard return value E_INVALIDARG as well as the following:




## -remarks



<b>FmtIdToPropStgName</b> maps a property set FMTID to its stream name for a simple property set or to its storage name for a nonsimple property set.

This function is useful in creating or opening a property set using the PROPSETFLAG_UNBUFFERED value with the 
<a href="https://msdn.microsoft.com/fc171888-3723-4894-a356-1b234352c4e8">StgCreatePropStg</a> and 
<a href="https://msdn.microsoft.com/ecc78e49-f1c2-4c2d-8390-b2b6f1dc776e">StgOpenPropStg</a> functions. For more information about PROPSETFLAG_UNBUFFERED, see <a href="https://msdn.microsoft.com/6f865c8f-bbca-4122-b076-14f2bc56f292">PROPSETFLAG Constants</a>.




## -see-also




<a href="https://msdn.microsoft.com/6f865c8f-bbca-4122-b076-14f2bc56f292">PROPSETFLAG Constants</a>



<a href="https://msdn.microsoft.com/bbbaf5a3-df17-42fd-ba2b-ad5b572c8a3f">PropStgNameToFmtId</a>



<a href="https://msdn.microsoft.com/fc171888-3723-4894-a356-1b234352c4e8">StgCreatePropStg</a>



<a href="https://msdn.microsoft.com/ecc78e49-f1c2-4c2d-8390-b2b6f1dc776e">StgOpenPropStg</a>
 

 

