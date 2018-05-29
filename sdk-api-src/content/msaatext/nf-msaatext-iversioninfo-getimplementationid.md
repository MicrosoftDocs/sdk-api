---
UID: NF:msaatext.IVersionInfo.GetImplementationID
title: IVersionInfo::GetImplementationID
author: windows-sdk-content
description: Clients call IVersionInfo::GetImplementationID to retrieve a unique identifier for the component.
old-location: winauto\iversioninfo_iversioninfo__getimplementationid.htm
old-project: WinAuto
ms.assetid: 018834df-bd03-4bf5-8af2-b325f7a6a586
ms.author: windowssdkdev
ms.date: 04/16/2018
ms.keywords: GetImplementationID, GetImplementationID method [Windows Accessibility], GetImplementationID method [Windows Accessibility],IVersionInfo interface, IVersionInfo interface [Windows Accessibility],GetImplementationID method, IVersionInfo.GetImplementationID, IVersionInfo::GetImplementationID, _msaa_IVersionInfo_GetImplementationID, msaa.iversioninfo_iversioninfo__getimplementationid, msaatext/IVersionInfo::GetImplementationID, winauto.iversioninfo_iversioninfo__getimplementationid
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
-	IVersionInfo.GetImplementationID
product: Windows
targetos: Windows
req.lib: 
req.dll: Msaatext.dll
req.irql: 
req.product: GDI+ 1.1
---

# IVersionInfo::GetImplementationID


## -description


Clients call <b>IVersionInfo::GetImplementationID</b> to retrieve a unique identifier for the component.
<div class="alert"><b>Note</b>  Active Accessibility Text Services is deprecated. Please see     
<a href="http://go.microsoft.com/fwlink/p/?linkid=131573">Microsoft Windows Text Services Framework</a>
for more information on advanced text input and natural language technologies.
		</div><div> </div>

## -parameters




### -param ulSub [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">ULONG</a></b>

The ordinal position of the component in the tree.


### -param implid [out]

Type: <b>GUID*</b>

An implementation identifier for the component. The implementation identifier is unique for this component and is used only for comparing components.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If successful, returns S_OK. If not successful, returns a standard <a href="https://msdn.microsoft.com/e6deca92-42da-41ab-bfdb-75cbce3022bb">COM error code</a>.



