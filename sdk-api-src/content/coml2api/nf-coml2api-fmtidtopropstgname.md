---
UID: NF:coml2api.FmtIdToPropStgName
title: FmtIdToPropStgName function (coml2api.h)

description: Converts a property set format identifier (FMTID) to its storage or stream name.
old-location: stg\fmtidtopropstgname.htm
tech.root: Stg
ms.assetid: 044f8883-bbd2-4cd3-b9dc-739ecb711bdd

ms.date: 12/05/2018
ms.keywords: FmtIdToPropStgName, FmtIdToPropStgName function [Structured Storage], _stg_fmtidtopropstgname, coml2api/FmtIdToPropStgName, stg.fmtidtopropstgname
ms.topic: function
f1_keywords: 
 - "coml2api/FmtIdToPropStgName"
dev_langs:
 - c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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
<a href="https://docs.microsoft.com/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropstg">StgCreatePropStg</a> and 
<a href="https://docs.microsoft.com/windows/desktop/api/coml2api/nf-coml2api-stgopenpropstg">StgOpenPropStg</a> functions. For more information about PROPSETFLAG_UNBUFFERED, see <a href="https://docs.microsoft.com/windows/desktop/Stg/propsetflag-constants">PROPSETFLAG Constants</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Stg/propsetflag-constants">PROPSETFLAG Constants</a>



<a href="https://docs.microsoft.com/windows/desktop/api/coml2api/nf-coml2api-propstgnametofmtid">PropStgNameToFmtId</a>



<a href="https://docs.microsoft.com/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropstg">StgCreatePropStg</a>



<a href="https://docs.microsoft.com/windows/desktop/api/coml2api/nf-coml2api-stgopenpropstg">StgOpenPropStg</a>
 

 

