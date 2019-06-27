---
UID: NF:gpedit.IGPEInformation.GetDisplayName
title: IGPEInformation::GetDisplayName (gpedit.h)
author: windows-sdk-content
description: The GetDisplayName method retrieves the display name for the GPO.
old-location: policy\igpeinformation_getdisplayname.htm
tech.root: Policy
ms.assetid: 3c1a43a5-5d16-4abc-85e0-1eeace2ee086
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetDisplayName, GetDisplayName method [Group Policy], GetDisplayName method [Group Policy],IGPEInformation interface, IGPEInformation interface [Group Policy],GetDisplayName method, IGPEInformation.GetDisplayName, IGPEInformation::GetDisplayName, _win32_igpeinformation_getdisplayname, gpedit/IGPEInformation::GetDisplayName, policy.igpeinformation_getdisplayname
ms.topic: method
f1_keywords: 
 - "gpedit/IGPEInformation.GetDisplayName"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gpedit.dll
api_name:
 - IGPEInformation.GetDisplayName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IGPEInformation::GetDisplayName


## -description


The
    <b>GetDisplayName</b> method retrieves the display name for the GPO.


## -parameters




### -param pszName [out]

Receives the display name for the GPO.


### -param cchMaxLength [in]

Specifies the size, in characters, of the <i>pszName</i> buffer.


## -returns



If the method succeeds, the return value is <b>S_OK</b>. Otherwise, the method returns one of the COM error codes defined in the Platform SDK header file WinError.h.




## -remarks



To retrieve the unique name for the GPO (typically a GUID), you can call the 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpedit/nf-gpedit-igpeinformation-getname">GetName</a> method.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpedit/nf-gpedit-igpeinformation-getname">GetName</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/Policy/group-policy-interfaces">Group Policy
    Interfaces</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/Policy/about-group-policy">Group Policy
    Overview</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpedit/nn-gpedit-igpeinformation">IGPEInformation</a>
 

 

