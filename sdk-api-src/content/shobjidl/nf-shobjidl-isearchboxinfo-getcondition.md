---
UID: NF:shobjidl.ISearchBoxInfo.GetCondition
title: ISearchBoxInfo::GetCondition (shobjidl.h)
description: Retrieves the contents of the search box as an ICondition object.
helpviewer_keywords: ["GetCondition","GetCondition method [Windows Shell]","GetCondition method [Windows Shell]","ISearchBoxInfo interface","ISearchBoxInfo interface [Windows Shell]","GetCondition method","ISearchBoxInfo.GetCondition","ISearchBoxInfo::GetCondition","_shell_ISearchBoxInfo_GetCondition","shell.ISearchBoxInfo_GetCondition","shobjidl/ISearchBoxInfo::GetCondition"]
old-location: shell\ISearchBoxInfo_GetCondition.htm
tech.root: shell
ms.assetid: 9a1159df-78ef-493b-8286-eefb0ac004ef
ms.date: 12/05/2018
ms.keywords: GetCondition, GetCondition method [Windows Shell], GetCondition method [Windows Shell],ISearchBoxInfo interface, ISearchBoxInfo interface [Windows Shell],GetCondition method, ISearchBoxInfo.GetCondition, ISearchBoxInfo::GetCondition, _shell_ISearchBoxInfo_GetCondition, shell.ISearchBoxInfo_GetCondition, shobjidl/ISearchBoxInfo::GetCondition
req.header: shobjidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
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
 - ISearchBoxInfo::GetCondition
 - shobjidl/ISearchBoxInfo::GetCondition
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shobjidl.h
api_name:
 - ISearchBoxInfo.GetCondition
---

# ISearchBoxInfo::GetCondition


## -description

Retrieves the contents of the search box as an <a href="/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-icondition">ICondition</a> object.

## -parameters

### -param riid [in]

Type: <b>REFIID</b>

A reference to the IID of the interface to retrieve through <i>ppv</i>, typically IID_ICondition.

### -param ppv [out]

Type: <b>void**</b>

When this method returns successfully, contains the interface pointer requested in <i>riid</i>. This is typically <a href="/windows/desktop/api/structuredquerycondition/nn-structuredquerycondition-icondition">ICondition</a>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

As opposed to the text string retrieved by <a href="/windows/desktop/api/shobjidl/nf-shobjidl-isearchboxinfo-gettext">ISearchBoxInfo::GetText</a>, <b>GetCondition</b> retrieves the same information as a structured object, the methods of which can be used to parse and manipulate the search string.

We recommend that you use the <b>IID_PPV_ARGS</b> macro, defined in Objbase.h, to package the <i>riid</i> and <i>ppv</i> parameters. This macro provides the correct IID based on the interface pointed to by the value in <i>ppv</i>, which eliminates the possibility of a coding error in <i>riid</i> that could lead to unexpected results.

## -see-also

<a href="/windows/desktop/api/shobjidl/nn-shobjidl-isearchboxinfo">ISearchBoxInfo</a>