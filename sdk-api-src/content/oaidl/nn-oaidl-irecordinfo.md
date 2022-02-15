---
UID: NN:oaidl.IRecordInfo
title: IRecordInfo (oaidl.h)
description: Describes the structure of a particular UDT.
helpviewer_keywords: ["IRecordInfo","IRecordInfo interface [Automation]","IRecordInfo interface [Automation]","described","_oa96_IRecordInfo_Interface","automat.irecordinfo","oaidl/IRecordInfo"]
old-location: automat\irecordinfo.htm
tech.root: automat
ms.assetid: 065ebfa8-bfac-4c75-a3f9-9dc0409ea454
ms.date: 12/05/2018
ms.keywords: IRecordInfo, IRecordInfo interface [Automation], IRecordInfo interface [Automation],described, _oa96_IRecordInfo_Interface, automat.irecordinfo, oaidl/IRecordInfo
req.header: oaidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OaIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IRecordInfo
 - oaidl/IRecordInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - oaidl.h
api_name:
 - IRecordInfo
---

# IRecordInfo interface


## -description

Describes the structure of a particular UDT. You can use <b>IRecordInfo</b> any time you need to access the description of UDTs contained in type libraries. <b>IRecordInfo</b> can be reused as needed; there can be many instances of the UDT for a single <b>IRecordInfo</b> pointer.

## -inheritance

The <b>IRecordInfo</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IRecordInfo</b> also has these types of members:

## -see-also

<a href="/previous-versions/windows/desktop/automat/udt-functions-and-interfaces">UDT Functions and Interfaces</a>



<a href="/previous-versions/windows/desktop/automat/user-defined-data-types">User-Defined Data Types </a>
