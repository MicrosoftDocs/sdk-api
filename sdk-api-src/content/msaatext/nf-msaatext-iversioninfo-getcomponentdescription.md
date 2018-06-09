---
UID: NF:msaatext.IVersionInfo.GetComponentDescription
title: IVersionInfo::GetComponentDescription
author: windows-sdk-content
description: Clients call this method to retrieve a description of the component.
old-location: winauto\iversioninfo_iversioninfo__getcomponentdescription.htm
old-project: WinAuto
ms.assetid: bb689adb-bd94-4c62-b408-33e1aa694c89
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: GetComponentDescription, GetComponentDescription method [Windows Accessibility], GetComponentDescription method [Windows Accessibility],IVersionInfo interface, IVersionInfo interface [Windows Accessibility],GetComponentDescription method, IVersionInfo.GetComponentDescription, IVersionInfo::GetComponentDescription, _msaa_IVersionInfo_GetComponentDescription, msaa.iversioninfo_iversioninfo__getcomponentdescription, msaatext/IVersionInfo::GetComponentDescription, winauto.iversioninfo_iversioninfo__getcomponentdescription
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
tech.root: 
req.typenames: SSTP_CONFIG_PARAMS, *PSSTP_CONFIG_PARAMS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msaatext.dll
api_name:
 - IVersionInfo.GetComponentDescription
product: Windows
targetos: Windows
req.lib: 
req.dll: Msaatext.dll
req.irql: 
req.product: GDI+ 1.1
---

# IVersionInfo::GetComponentDescription


## -description


Clients call this method to retrieve a description of the component.
		
<div class="alert"><b>Note</b>  Active Accessibility Text Services is deprecated. Please see     
<a href="http://go.microsoft.com/fwlink/p/?linkid=131573">Microsoft Windows Text Services Framework</a>
for more information on advanced text input and natural language technologies.
		</div><div> </div>

## -parameters




### -param ulSub [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">ULONG</a></b>

The ordinal position of the component in the tree.


### -param pImplStr [out]

Type: <b>BSTR*</b>

String of the form of "Company, suite, component, version." This is for human consumption and is not expected to be 
			 parsed.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If successful, returns S_OK. If not successful, returns a standard <a href="https://msdn.microsoft.com/e6deca92-42da-41ab-bfdb-75cbce3022bb">COM error code</a>.



