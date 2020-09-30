---
UID: NF:gpedit.IGPEInformation.GetOptions
title: IGPEInformation::GetOptions (gpedit.h)
description: The GetOptions method retrieves the options the user has selected for the Group Policy Object Editor.
helpviewer_keywords: ["GetOptions","GetOptions method [Group Policy]","GetOptions method [Group Policy]","IGPEInformation interface","IGPEInformation interface [Group Policy]","GetOptions method","IGPEInformation.GetOptions","IGPEInformation::GetOptions","_win32_igpeinformation_getoptions","gpedit/IGPEInformation::GetOptions","policy.igpeinformation_getoptions"]
old-location: policy\igpeinformation_getoptions.htm
tech.root: Policy
ms.assetid: 22c90ec4-b4cc-4a95-becd-29c2ce6e3c29
ms.date: 12/05/2018
ms.keywords: GetOptions, GetOptions method [Group Policy], GetOptions method [Group Policy],IGPEInformation interface, IGPEInformation interface [Group Policy],GetOptions method, IGPEInformation.GetOptions, IGPEInformation::GetOptions, _win32_igpeinformation_getoptions, gpedit/IGPEInformation::GetOptions, policy.igpeinformation_getoptions
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
 - IGPEInformation::GetOptions
 - gpedit/IGPEInformation::GetOptions
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
 - IGPEInformation.GetOptions
---

# IGPEInformation::GetOptions


## -description

The
    <b>GetOptions</b> method retrieves the options the user has selected for the Group Policy Object Editor.

## -parameters

### -param dwOptions [out]

Receives a bitmask value representing the options the user has selected. Currently, this parameter returns only zero.

## -returns

If the method succeeds, the return value is <b>S_OK</b>. Otherwise, the method returns one of the COM error codes defined in the Platform SDK header file WinError.h.

## -see-also

<a href="/previous-versions/windows/desktop/Policy/group-policy-interfaces">Group Policy
    Interfaces</a>



<a href="/previous-versions/windows/desktop/Policy/about-group-policy">Group Policy
    Overview</a>



<a href="/previous-versions/windows/desktop/api/gpedit/nn-gpedit-igpeinformation">IGPEInformation</a>