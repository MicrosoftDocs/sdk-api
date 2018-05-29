---
UID: NF:msaatext.IVersionInfo.GetBuildVersion
title: IVersionInfo::GetBuildVersion
author: windows-sdk-content
description: Clients call IVersionInfo::GetBuildVersion to retrieve build information for a specified component.
old-location: winauto\iversioninfo_iversioninfo__getbuildversion.htm
old-project: WinAuto
ms.assetid: ae54ad59-665c-494c-8054-3f19aec9968f
ms.author: windowssdkdev
ms.date: 04/16/2018
ms.keywords: GetBuildVersion, GetBuildVersion method [Windows Accessibility], GetBuildVersion method [Windows Accessibility],IVersionInfo interface, IVersionInfo interface [Windows Accessibility],GetBuildVersion method, IVersionInfo.GetBuildVersion, IVersionInfo::GetBuildVersion, _msaa_IVersionInfo_GetBuildVersion, msaa.iversioninfo_iversioninfo__getbuildversion, msaatext/IVersionInfo::GetBuildVersion, winauto.iversioninfo_iversioninfo__getbuildversion
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
req.typenames: SSTP_CONFIG_PARAMS, *PSSTP_CONFIG_PARAMS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	msaatext.dll
api_name:
-	IVersionInfo.GetBuildVersion
product: Windows
targetos: Windows
req.lib: 
req.dll: Msaatext.dll
req.irql: 
req.product: GDI+ 1.1
---

# IVersionInfo::GetBuildVersion


## -description


Clients call <b>IVersionInfo::GetBuildVersion</b> to retrieve build information for a specified component.
<div class="alert"><b>Note</b>  Active Accessibility Text Services is deprecated. Please see     
<a href="http://go.microsoft.com/fwlink/p/?linkid=131573">Microsoft Windows Text Services Framework</a>
for more information on advanced text input and natural language technologies.
		</div><div> </div>

## -parameters




### -param ulSub [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">ULONG</a></b>

The ordinal position of the component in the tree.


### -param pdwMajor [out]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a>*</b>

The major build version of the component specified in <i>ulSub</i>.


### -param pdwMinor [out]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a>*</b>

The minor build version of the component specified in <i>ulSub</i>.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If successful, returns S_OK. If not successful, returns a standard <a href="https://msdn.microsoft.com/e6deca92-42da-41ab-bfdb-75cbce3022bb">COM error code</a>.



