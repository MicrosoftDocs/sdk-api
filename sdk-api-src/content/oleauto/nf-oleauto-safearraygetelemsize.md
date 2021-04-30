---
UID: NF:oleauto.SafeArrayGetElemsize
title: SafeArrayGetElemsize function (oleauto.h)
description: Gets the size of an element.
helpviewer_keywords: ["SafeArrayGetElemsize","SafeArrayGetElemsize function [Automation]","_oa96_SafeArrayGetElemsize","automat.safearraygetelemsize","oleauto/SafeArrayGetElemsize"]
old-location: automat\safearraygetelemsize.htm
tech.root: automat
ms.assetid: 27bd4a3f-0e9d-45f7-ad7c-0c0b59579dd0
ms.date: 12/05/2018
ms.keywords: SafeArrayGetElemsize, SafeArrayGetElemsize function [Automation], _oa96_SafeArrayGetElemsize, automat.safearraygetelemsize, oleauto/SafeArrayGetElemsize
req.header: oleauto.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: OleAut32.lib
req.dll: OleAut32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SafeArrayGetElemsize
 - oleauto/SafeArrayGetElemsize
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - OleAut32.dll
api_name:
 - SafeArrayGetElemsize
---

# SafeArrayGetElemsize function


## -description

Gets the size of an element.

## -parameters

### -param psa [in]

An array descriptor created by <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-safearraycreate">SafeArrayCreate</a>.

## -returns

The size of an element in a safe array, in bytes.