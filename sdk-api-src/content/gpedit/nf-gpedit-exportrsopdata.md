---
UID: NF:gpedit.ExportRSoPData
title: ExportRSoPData function (gpedit.h)
description: The ExportRSoPData function exports a WMI namespace that contains RSoP information to a data file. The function writes the information to a data file that can be imported to a WMI namespace with a call to the ImportRSoPData function.
helpviewer_keywords: ["ExportRSoPData","ExportRSoPData function [Group Policy]","_win32_exportrsopdata","gpedit/ExportRSoPData","policy.exportrsopdata"]
old-location: policy\exportrsopdata.htm
tech.root: Policy
ms.assetid: a3f20a35-8d9c-403b-ba76-24c8b3640c6d
ms.date: 12/05/2018
ms.keywords: ExportRSoPData, ExportRSoPData function [Group Policy], _win32_exportrsopdata, gpedit/ExportRSoPData, policy.exportrsopdata
req.header: gpedit.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Gpedit.lib
req.dll: Gpedit.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ExportRSoPData
 - gpedit/ExportRSoPData
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Gpedit.dll
api_name:
 - ExportRSoPData
---

# ExportRSoPData function


## -description

The
    <b>ExportRSoPData</b> function exports a WMI namespace that contains RSoP information to a data file. The function writes the information to a data file that can be imported to a WMI namespace with a call to the 
<a href="/previous-versions/windows/desktop/api/gpedit/nf-gpedit-importrsopdata">ImportRSoPData</a> function.

## -parameters

### -param lpNameSpace [in]

A pointer to a string that specifies the namespace which contains the RSoP data.

### -param lpFileName [in]

A pointer to a string that specifies the name of the file to receive the RSoP data.

## -returns

If the function succeeds, the return value is <b>S_OK</b>. Otherwise, the function returns one of the COM error codes defined in the header file WinError.h.

## -remarks

It is recommended that you call the 
<b>ExportRSoPData</b> function twice: one time to process the user data and a second time to process the computer data.

## -see-also

<a href="/previous-versions/windows/desktop/Policy/group-policy-functions">Group Policy
    Functions</a>



<a href="/previous-versions/windows/desktop/Policy/about-group-policy">Group Policy
    Overview</a>



<a href="/previous-versions/windows/desktop/api/gpedit/nf-gpedit-importrsopdata">ImportRSoPData</a>