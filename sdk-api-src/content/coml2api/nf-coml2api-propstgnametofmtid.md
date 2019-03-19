---
UID: NF:coml2api.PropStgNameToFmtId
title: PropStgNameToFmtId function (coml2api.h)
author: windows-sdk-content
description: Converts a property set storage or stream name to its format identifier.
old-location: stg\propstgnametofmtid.htm
tech.root: Stg
ms.assetid: bbbaf5a3-df17-42fd-ba2b-ad5b572c8a3f
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: PropStgNameToFmtId, PropStgNameToFmtId function [Structured Storage], _stg_propstgnametofmtid, coml2api/PropStgNameToFmtId, stg.propstgnametofmtid
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
 - PropStgNameToFmtId
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
<a href="https://msdn.microsoft.com/fc171888-3723-4894-a356-1b234352c4e8">StgCreatePropStg</a> and 
<a href="https://msdn.microsoft.com/ecc78e49-f1c2-4c2d-8390-b2b6f1dc776e">StgOpenPropStg</a> functions. For more information about PROPSETFLAG_UNBUFFERED, see <a href="https://msdn.microsoft.com/6f865c8f-bbca-4122-b076-14f2bc56f292">PROPSETFLAG Constants</a>.




## -see-also




<a href="https://msdn.microsoft.com/044f8883-bbd2-4cd3-b9dc-739ecb711bdd">FmtIdToPropStgName</a>



<a href="https://msdn.microsoft.com/6f865c8f-bbca-4122-b076-14f2bc56f292">PROPSETFLAG Constants</a>



<a href="https://msdn.microsoft.com/fc171888-3723-4894-a356-1b234352c4e8">StgCreatePropStg</a>



<a href="https://msdn.microsoft.com/ecc78e49-f1c2-4c2d-8390-b2b6f1dc776e">StgOpenPropStg</a>
 

 

