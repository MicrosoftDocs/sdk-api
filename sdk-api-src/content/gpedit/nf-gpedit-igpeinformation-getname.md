---
UID: NF:gpedit.IGPEInformation.GetName
title: IGPEInformation::GetName (gpedit.h)
description: The GetName method retrieves the unique name for the GPO. This value is usually a GUID.
helpviewer_keywords: ["GetName","GetName method [Group Policy]","GetName method [Group Policy]","IGPEInformation interface","IGPEInformation interface [Group Policy]","GetName method","IGPEInformation.GetName","IGPEInformation::GetName","_win32_igpeinformation_getname","gpedit/IGPEInformation::GetName","policy.igpeinformation_getname"]
old-location: policy\igpeinformation_getname.htm
tech.root: Policy
ms.assetid: 94112a6e-cd8a-4fb7-9c37-86a1b7713ddb
ms.date: 12/05/2018
ms.keywords: GetName, GetName method [Group Policy], GetName method [Group Policy],IGPEInformation interface, IGPEInformation interface [Group Policy],GetName method, IGPEInformation.GetName, IGPEInformation::GetName, _win32_igpeinformation_getname, gpedit/IGPEInformation::GetName, policy.igpeinformation_getname
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
 - IGPEInformation::GetName
 - gpedit/IGPEInformation::GetName
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
 - IGPEInformation.GetName
---

# IGPEInformation::GetName


## -description

The
    <b>GetName</b> method retrieves the unique name for the GPO. This value is usually a GUID.

## -parameters

### -param pszName [out]

Receives the GPO name.

### -param cchMaxLength [in]

Specifies the size, in characters, of the <i>pszName</i> buffer.

## -returns

If the method succeeds, the return value is <b>S_OK</b>. Otherwise, the method returns one of the COM error codes defined in the Platform SDK header file WinError.h.

## -remarks

To retrieve the GPO's friendly name, which is suitable for display, you can call the 
<a href="/previous-versions/windows/desktop/api/gpedit/nf-gpedit-igpeinformation-getdisplayname">GetDisplayName</a> method.

## -see-also

<a href="/previous-versions/windows/desktop/api/gpedit/nf-gpedit-igpeinformation-getdisplayname">GetDisplayName</a>



<a href="/previous-versions/windows/desktop/Policy/group-policy-interfaces">Group Policy
    Interfaces</a>



<a href="/previous-versions/windows/desktop/Policy/about-group-policy">Group Policy
    Overview</a>



<a href="/previous-versions/windows/desktop/api/gpedit/nn-gpedit-igpeinformation">IGPEInformation</a>