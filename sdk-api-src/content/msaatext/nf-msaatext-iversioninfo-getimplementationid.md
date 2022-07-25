---
UID: NF:msaatext.IVersionInfo.GetImplementationID
title: IVersionInfo::GetImplementationID (msaatext.h)
description: Clients call IVersionInfo::GetImplementationID to retrieve a unique identifier for the component.
helpviewer_keywords: ["GetImplementationID","GetImplementationID method [Windows Accessibility]","GetImplementationID method [Windows Accessibility]","IVersionInfo interface","IVersionInfo interface [Windows Accessibility]","GetImplementationID method","IVersionInfo.GetImplementationID","IVersionInfo::GetImplementationID","_msaa_IVersionInfo_GetImplementationID","msaa.iversioninfo_iversioninfo__getimplementationid","msaatext/IVersionInfo::GetImplementationID","winauto.iversioninfo_iversioninfo__getimplementationid"]
old-location: winauto\iversioninfo_iversioninfo__getimplementationid.htm
tech.root: WinAuto
ms.assetid: 018834df-bd03-4bf5-8af2-b325f7a6a586
ms.date: 12/05/2018
ms.keywords: GetImplementationID, GetImplementationID method [Windows Accessibility], GetImplementationID method [Windows Accessibility],IVersionInfo interface, IVersionInfo interface [Windows Accessibility],GetImplementationID method, IVersionInfo.GetImplementationID, IVersionInfo::GetImplementationID, _msaa_IVersionInfo_GetImplementationID, msaa.iversioninfo_iversioninfo__getimplementationid, msaatext/IVersionInfo::GetImplementationID, winauto.iversioninfo_iversioninfo__getimplementationid
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
 - IVersionInfo::GetImplementationID
 - msaatext/IVersionInfo::GetImplementationID
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
 - IVersionInfo.GetImplementationID
---

# IVersionInfo::GetImplementationID


## -description

Clients call <b>IVersionInfo::GetImplementationID</b> to retrieve a unique identifier for the component.
<div class="alert"><b>Note</b>  Active Accessibility Text Services is deprecated. Please see     
<a href="/windows/win32/tsf/text-services-framework">Microsoft Windows Text Services Framework</a> for more information on advanced text input and natural language technologies.
		</div><div> </div>

## -parameters

### -param ulSub [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">ULONG</a></b>

The ordinal position of the component in the tree.

### -param implid [out]

Type: <b>GUID*</b>

An implementation identifier for the component. The implementation identifier is unique for this component and is used only for comparing components.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If successful, returns S_OK. If not successful, returns a standard <a href="/windows/desktop/WinAuto/return-values">COM error code</a>.