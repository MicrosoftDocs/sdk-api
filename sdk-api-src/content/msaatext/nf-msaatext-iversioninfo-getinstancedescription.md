---
UID: NF:msaatext.IVersionInfo.GetInstanceDescription
title: IVersionInfo::GetInstanceDescription (msaatext.h)
description: Clients call this method to retrieve a description of the instance.Note  Active Accessibility Text Services is deprecated.
helpviewer_keywords: ["GetInstanceDescription","GetInstanceDescription method [Windows Accessibility]","GetInstanceDescription method [Windows Accessibility]","IVersionInfo interface","IVersionInfo interface [Windows Accessibility]","GetInstanceDescription method","IVersionInfo.GetInstanceDescription","IVersionInfo::GetInstanceDescription","_msaa_IVersionInfo_GetInstanceDescription","msaa.iversioninfo_iversioninfo__getinstancedescription","msaatext/IVersionInfo::GetInstanceDescription","winauto.iversioninfo_iversioninfo__getinstancedescription"]
old-location: winauto\iversioninfo_iversioninfo__getinstancedescription.htm
tech.root: WinAuto
ms.assetid: f8aa3fd3-9869-4c24-8c9a-752947d21002
ms.date: 12/05/2018
ms.keywords: GetInstanceDescription, GetInstanceDescription method [Windows Accessibility], GetInstanceDescription method [Windows Accessibility],IVersionInfo interface, IVersionInfo interface [Windows Accessibility],GetInstanceDescription method, IVersionInfo.GetInstanceDescription, IVersionInfo::GetInstanceDescription, _msaa_IVersionInfo_GetInstanceDescription, msaa.iversioninfo_iversioninfo__getinstancedescription, msaatext/IVersionInfo::GetInstanceDescription, winauto.iversioninfo_iversioninfo__getinstancedescription
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
 - IVersionInfo::GetInstanceDescription
 - msaatext/IVersionInfo::GetInstanceDescription
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
 - IVersionInfo.GetInstanceDescription
---

# IVersionInfo::GetInstanceDescription


## -description

Clients call this method to retrieve a description of the instance.
<div class="alert"><b>Note</b>  Active Accessibility Text Services is deprecated. Please see     
<a href="/windows/win32/tsf/text-services-framework">Microsoft Windows Text Services Framework</a> for more information on advanced text input and natural language technologies.
		</div><div> </div>

## -parameters

### -param ulSub [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">ULONG</a></b>

The ordinal position of the component in the tree.

### -param pImplStr [out]

Type: <b>BSTR*</b>

Additional useful strings for the component, such as the internal object state.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If successful, returns S_OK. If not successful, returns a standard <a href="/windows/desktop/WinAuto/return-values">COM error code</a>.