---
UID: NF:gpedit.BrowseForGPO
title: BrowseForGPO function (gpedit.h)
description: The BrowseForGPO function creates a GPO browser dialog box that allows the user to open or create a GPO.
helpviewer_keywords: ["BrowseForGPO","BrowseForGPO function [Group Policy]","_win32_browseforgpo","gpedit/BrowseForGPO","policy.browseforgpo"]
old-location: policy\browseforgpo.htm
tech.root: Policy
ms.assetid: ff144ae4-fc8c-499e-9086-75625b86693c
ms.date: 12/05/2018
ms.keywords: BrowseForGPO, BrowseForGPO function [Group Policy], _win32_browseforgpo, gpedit/BrowseForGPO, policy.browseforgpo
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
 - BrowseForGPO
 - gpedit/BrowseForGPO
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
 - BrowseForGPO
---

# BrowseForGPO function


## -description

The
    <b>BrowseForGPO</b> function creates a GPO browser dialog box that allows the user to open or create a GPO.

## -parameters

### -param lpBrowseInfo [in, out]

A pointer to a 
<a href="/windows/win32/api/gpedit/ns-gpedit-gpobrowseinfo">GPOBROWSEINFO</a> structure that contains information used to initialize the dialog box. When 
the <b>BrowseForGPO</b> function returns, this structure contains information about the user's actions.

## -returns

If the function succeeds, the return value is <b>S_OK</b>. If the user cancels or closes the dialog box, the return value is <b>HRESULT_FROM_WIN32</b>(<b>ERROR_CANCELLED</b>). Otherwise, the function returns one of the COM error codes defined in the header file WinError.h.

## -see-also

<a href="/windows/win32/api/gpedit/ns-gpedit-gpobrowseinfo">GPOBROWSEINFO</a>



<a href="/previous-versions/windows/desktop/Policy/group-policy-functions">Group Policy
    Functions</a>



<a href="/previous-versions/windows/desktop/Policy/about-group-policy">Group Policy
    Overview</a>