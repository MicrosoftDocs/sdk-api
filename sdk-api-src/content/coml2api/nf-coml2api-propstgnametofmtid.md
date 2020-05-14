---
UID: NF:coml2api.PropStgNameToFmtId
title: PropStgNameToFmtId function (coml2api.h)
description: Converts a property set storage or stream name to its format identifier.helpviewer_keywords: ["PropStgNameToFmtId","PropStgNameToFmtId function [Structured Storage]","_stg_propstgnametofmtid","coml2api/PropStgNameToFmtId","stg.propstgnametofmtid"]
old-location: stg\propstgnametofmtid.htm
tech.root: Stg
ms.assetid: bbbaf5a3-df17-42fd-ba2b-ad5b572c8a3f
ms.date: 12/05/2018
ms.keywords: PropStgNameToFmtId, PropStgNameToFmtId function [Structured Storage], _stg_propstgnametofmtid, coml2api/PropStgNameToFmtId, stg.propstgnametofmtid
f1_keywords:
- coml2api/PropStgNameToFmtId
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
- PropStgNameToFmtId
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PropStgNameToFmtId function


## -description


The <b>PropStgNameToFmtId</b> function converts a property set storage or stream name to its format identifier.


## -parameters




### -param oszName [in]

A pointer to a null-terminated Unicode string that contains the stream name of a simple property set or the storage name of a nonsimple property set.


### -param pfmtid [out]

A pointer to a FMTID variable that receives the format identifier of the property set specified by <i>oszName</i>.


## -returns



This function supports the standard return value E_INVALIDARG as well as the following:




## -remarks



The <b>PropStgNameToFmtId</b> function maps the stream name of a simple property set or the storage name of a nonsimple property set to its format identifier.

This function is useful in creating or opening a property set using the PROPSETFLAG_UNBUFFERED value with the 
<a href="https://docs.microsoft.com/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropstg">StgCreatePropStg</a> and 
<a href="https://docs.microsoft.com/windows/desktop/api/coml2api/nf-coml2api-stgopenpropstg">StgOpenPropStg</a> functions. For more information about PROPSETFLAG_UNBUFFERED, see <a href="https://docs.microsoft.com/windows/desktop/Stg/propsetflag-constants">PROPSETFLAG Constants</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/coml2api/nf-coml2api-fmtidtopropstgname">FmtIdToPropStgName</a>



<a href="https://docs.microsoft.com/windows/desktop/Stg/propsetflag-constants">PROPSETFLAG Constants</a>



<a href="https://docs.microsoft.com/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropstg">StgCreatePropStg</a>



<a href="https://docs.microsoft.com/windows/desktop/api/coml2api/nf-coml2api-stgopenpropstg">StgOpenPropStg</a>
 

 

