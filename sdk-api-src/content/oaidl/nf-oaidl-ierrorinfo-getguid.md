---
UID: NF:oaidl.IErrorInfo.GetGUID
title: IErrorInfo::GetGUID (oaidl.h)
description: Returns the globally unique identifier (GUID) of the interface that defined the error.
helpviewer_keywords: ["GetGUID","GetGUID method [Automation]","GetGUID method [Automation]","IErrorInfo interface","IErrorInfo interface [Automation]","GetGUID method","IErrorInfo.GetGUID","IErrorInfo::GetGUID","_oa96_IErrorInfo_GetGUID","automat.ierrorinfo_getguid","oaidl/IErrorInfo::GetGUID"]
old-location: automat\ierrorinfo_getguid.htm
tech.root: automat
ms.assetid: a4223508-6e8b-41b7-b808-a0d883bc265b
ms.date: 12/05/2018
ms.keywords: GetGUID, GetGUID method [Automation], GetGUID method [Automation],IErrorInfo interface, IErrorInfo interface [Automation],GetGUID method, IErrorInfo.GetGUID, IErrorInfo::GetGUID, _oa96_IErrorInfo_GetGUID, automat.ierrorinfo_getguid, oaidl/IErrorInfo::GetGUID
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
 - IErrorInfo::GetGUID
 - oaidl/IErrorInfo::GetGUID
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
 - IErrorInfo.GetGUID
---

# IErrorInfo::GetGUID


## -description

Returns the globally unique identifier (GUID) of the interface that defined the error.

## -parameters

### -param pGUID [out]

A pointer to a GUID, or GUID_NULL, if the error was defined by the operating system.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

<b>IErrorInfo::GetGUID</b> returns the GUID of the interface that defined the error. If the error was defined by the system, <b>IErrorInfo::GetGUID</b> returns GUID_NULL.



This GUID does not necessarily represent the source of the error. The source is the class or application that raised the error. Using the GUID, an application can handle errors in an interface, independent of the class that implements the interface.

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ierrorinfo">IErrorInfo</a>