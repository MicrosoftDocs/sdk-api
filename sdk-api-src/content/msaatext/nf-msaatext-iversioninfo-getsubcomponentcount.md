---
UID: NF:msaatext.IVersionInfo.GetSubcomponentCount
title: IVersionInfo::GetSubcomponentCount method
author: windows-driver-content
description: Clients call IVersionInfo::GetSubcomponentCount to determine the number of subcomponents for which version information is returned.
old-location: winauto\iversioninfo_iversioninfo__getsubcomponentcount.htm
old-project: WinAuto
ms.assetid: d1a169f1-db47-4c5b-9515-1f2660cfae17
ms.author: windowsdriverdev
ms.date: 4/16/2018
ms.keywords: GetSubcomponentCount method [Windows Accessibility], GetSubcomponentCount method [Windows Accessibility], IVersionInfo interface, GetSubcomponentCount,IVersionInfo.GetSubcomponentCount, IVersionInfo, IVersionInfo interface [Windows Accessibility], GetSubcomponentCount method, IVersionInfo::GetSubcomponentCount, _msaa_IVersionInfo_GetSubcomponentCount, msaa.iversioninfo_iversioninfo__getsubcomponentcount, msaatext/IVersionInfo::GetSubcomponentCount, winauto.iversioninfo_iversioninfo__getsubcomponentcount
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: msaatext.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
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
-	IVersionInfo.GetSubcomponentCount
product: Windows
targetos: Windows
req.lib: 
req.dll: Msaatext.dll
req.irql: 
req.product: GDI+ 1.1
---

# IVersionInfo::GetSubcomponentCount method


## -description


Clients call <b>IVersionInfo::GetSubcomponentCount</b> 
		to determine the number of subcomponents for which version information is returned.
<div class="alert"><b>Note</b>  Active Accessibility Text Services is deprecated. Please see     
<a href="http://go.microsoft.com/fwlink/p/?linkid=131573">Microsoft Windows Text Services Framework</a>
for more information on advanced text input and natural language technologies.
		</div><div> </div>

## -parameters




### -param ulSub [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">ULONG</a></b>

The ordinal position of the component in the tree.


### -param ulCount [out]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">ULONG</a>*</b>

The number of subcomponents that this component will expose version information about.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If successful, returns S_OK. If not successful, returns a standard <a href="https://msdn.microsoft.com/e6deca92-42da-41ab-bfdb-75cbce3022bb">COM error code</a>.



