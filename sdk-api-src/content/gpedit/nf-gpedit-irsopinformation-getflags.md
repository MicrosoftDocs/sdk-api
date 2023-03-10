---
UID: NF:gpedit.IRSOPInformation.GetFlags
title: IRSOPInformation::GetFlags (gpedit.h)
description: The GetFlags method retrieves information about the RSoP user interface session.
helpviewer_keywords: ["GetFlags","GetFlags method [Group Policy]","GetFlags method [Group Policy]","IRSOPInformation interface","IRSOPInformation interface [Group Policy]","GetFlags method","IRSOPInformation.GetFlags","IRSOPInformation::GetFlags","RSOP_INFO_FLAG_LOGGING_MODE","_win32_irsopinformation_getflags","gpedit/IRSOPInformation::GetFlags","policy.irsopinformation_getflags"]
old-location: policy\irsopinformation_getflags.htm
tech.root: Policy
ms.assetid: 10a518a3-9097-4efd-90cc-14ea66b70fa2
ms.date: 12/05/2018
ms.keywords: GetFlags, GetFlags method [Group Policy], GetFlags method [Group Policy],IRSOPInformation interface, IRSOPInformation interface [Group Policy],GetFlags method, IRSOPInformation.GetFlags, IRSOPInformation::GetFlags, RSOP_INFO_FLAG_LOGGING_MODE, _win32_irsopinformation_getflags, gpedit/IRSOPInformation::GetFlags, policy.irsopinformation_getflags
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
req.lib: 
req.dll: Gpedit.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IRSOPInformation::GetFlags
 - gpedit/IRSOPInformation::GetFlags
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gpedit.dll
api_name:
 - IRSOPInformation.GetFlags
---

# IRSOPInformation::GetFlags


## -description

The
    <b>GetFlags</b> method retrieves information about the RSoP user interface session.

## -parameters

### -param pdwFlags [out]

Receives a pointer to a value that contains information about the RSoP session. This parameter can be the following value.



#### RSOP_INFO_FLAG_LOGGING_MODE

If this value is specified, the RSoP session is in logging mode. If this value is not specified, it indicates that the session is in planning mode.

## -returns

If the method succeeds, the return value is <b>S_OK</b>. Otherwise, the method returns one of the COM error codes defined in the Platform SDK header file WinError.h.

## -see-also

<a href="/previous-versions/windows/desktop/Policy/group-policy-interfaces">Group Policy
    Interfaces</a>



<a href="/previous-versions/windows/desktop/Policy/about-group-policy">Group Policy
    Overview</a>



<a href="/previous-versions/windows/desktop/api/gpedit/nn-gpedit-irsopinformation">IRSOPInformation</a>