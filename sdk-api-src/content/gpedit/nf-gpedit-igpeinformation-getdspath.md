---
UID: NF:gpedit.IGPEInformation.GetDSPath
title: IGPEInformation::GetDSPath (gpedit.h)
description: The GetDSPath method retrieves the Active Directory path for the specified section of the GPO.
helpviewer_keywords: ["GPO_SECTION_MACHINE","GPO_SECTION_ROOT","GPO_SECTION_USER","GetDSPath","GetDSPath method [Group Policy]","GetDSPath method [Group Policy]","IGPEInformation interface","IGPEInformation interface [Group Policy]","GetDSPath method","IGPEInformation.GetDSPath","IGPEInformation::GetDSPath","_win32_igpeinformation_getdspath","gpedit/IGPEInformation::GetDSPath","policy.igpeinformation_getdspath"]
old-location: policy\igpeinformation_getdspath.htm
tech.root: Policy
ms.assetid: 0cf969b2-40a9-4fbd-ba2b-38979fb5796a
ms.date: 12/05/2018
ms.keywords: GPO_SECTION_MACHINE, GPO_SECTION_ROOT, GPO_SECTION_USER, GetDSPath, GetDSPath method [Group Policy], GetDSPath method [Group Policy],IGPEInformation interface, IGPEInformation interface [Group Policy],GetDSPath method, IGPEInformation.GetDSPath, IGPEInformation::GetDSPath, _win32_igpeinformation_getdspath, gpedit/IGPEInformation::GetDSPath, policy.igpeinformation_getdspath
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
 - IGPEInformation::GetDSPath
 - gpedit/IGPEInformation::GetDSPath
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
 - IGPEInformation.GetDSPath
---

# IGPEInformation::GetDSPath


## -description

The
    <b>GetDSPath</b> method retrieves the Active Directory path for the specified section of the GPO.

## -parameters

### -param dwSection [in]

Specifies the GPO section. This parameter can be one of the following values.



#### GPO_SECTION_ROOT

Root section



#### GPO_SECTION_USER

User section



#### GPO_SECTION_MACHINE

Computer section

### -param pszPath [out]

Receives the Active Directory path to the root of the requested section. For more information, see the following Remarks section.

### -param cchMaxPath [in]

Specifies the size, in characters, of the <i>pszPath</i> parameter.

## -returns

If the method succeeds, the return value is <b>S_OK</b>. Otherwise, the method returns one of the COM error codes defined in the Platform SDK header file WinError.h.

## -remarks

If you call the 
<b>GetDSPath</b> method and specify a computer GPO, the method succeeds, but on return, the <i>pszPath</i> parameter contains an empty string. This is because computer GPOs do not have Active Directory storage; they have only file system storage.

To retrieve the file system path for the specified section of a GPO, you can call the 
<a href="/previous-versions/windows/desktop/api/gpedit/nf-gpedit-igpeinformation-getfilesyspath">GetFileSysPath</a> method.

## -see-also

<a href="/previous-versions/windows/desktop/api/gpedit/nf-gpedit-igpeinformation-getfilesyspath">GetFileSysPath</a>



<a href="/previous-versions/windows/desktop/Policy/group-policy-interfaces">Group Policy
    Interfaces</a>



<a href="/previous-versions/windows/desktop/Policy/about-group-policy">Group Policy
    Overview</a>



<a href="/previous-versions/windows/desktop/api/gpedit/nn-gpedit-igpeinformation">IGPEInformation</a>