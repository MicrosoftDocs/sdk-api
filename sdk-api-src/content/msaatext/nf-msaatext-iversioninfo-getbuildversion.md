---
UID: NF:msaatext.IVersionInfo.GetBuildVersion
title: IVersionInfo::GetBuildVersion (msaatext.h)
description: Clients call IVersionInfo::GetBuildVersion to retrieve build information for a specified component.
helpviewer_keywords: ["GetBuildVersion","GetBuildVersion method [Windows Accessibility]","GetBuildVersion method [Windows Accessibility]","IVersionInfo interface","IVersionInfo interface [Windows Accessibility]","GetBuildVersion method","IVersionInfo.GetBuildVersion","IVersionInfo::GetBuildVersion","_msaa_IVersionInfo_GetBuildVersion","msaa.iversioninfo_iversioninfo__getbuildversion","msaatext/IVersionInfo::GetBuildVersion","winauto.iversioninfo_iversioninfo__getbuildversion"]
old-location: winauto\iversioninfo_iversioninfo__getbuildversion.htm
tech.root: WinAuto
ms.assetid: ae54ad59-665c-494c-8054-3f19aec9968f
ms.date: 12/05/2018
ms.keywords: GetBuildVersion, GetBuildVersion method [Windows Accessibility], GetBuildVersion method [Windows Accessibility],IVersionInfo interface, IVersionInfo interface [Windows Accessibility],GetBuildVersion method, IVersionInfo.GetBuildVersion, IVersionInfo::GetBuildVersion, _msaa_IVersionInfo_GetBuildVersion, msaa.iversioninfo_iversioninfo__getbuildversion, msaatext/IVersionInfo::GetBuildVersion, winauto.iversioninfo_iversioninfo__getbuildversion
req.header: msaatext.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.dll: Msaatext.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Active Accessibility 2.0 RDK on Windows NT 4.0 with SP6 and later and Windows 98
ms.custom: 19H1
f1_keywords:
 - IVersionInfo::GetBuildVersion
 - msaatext/IVersionInfo::GetBuildVersion
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msaatext.dll
api_name:
 - IVersionInfo.GetBuildVersion
---

# IVersionInfo::GetBuildVersion


## -description

Clients call <b>IVersionInfo::GetBuildVersion</b> to retrieve build information for a specified component.
<div class="alert"><b>Note</b>  Active Accessibility Text Services is deprecated. Please see     
<a href="/windows/win32/tsf/text-services-framework">Microsoft Windows Text Services Framework</a> for more information on advanced text input and natural language technologies.
		</div><div> </div>

## -parameters

### -param ulSub [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">ULONG</a></b>

The ordinal position of the component in the tree.

### -param pdwMajor [out]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a>*</b>

The major build version of the component specified in <i>ulSub</i>.

### -param pdwMinor [out]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a>*</b>

The minor build version of the component specified in <i>ulSub</i>.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If successful, returns S_OK. If not successful, returns a standard <a href="/windows/desktop/WinAuto/return-values">COM error code</a>.