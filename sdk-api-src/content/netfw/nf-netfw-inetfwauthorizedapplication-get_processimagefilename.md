---
UID: NF:netfw.INetFwAuthorizedApplication.get_ProcessImageFileName
title: INetFwAuthorizedApplication::get_ProcessImageFileName (netfw.h)
description: Specifies the process image file name for this application. (Get)
helpviewer_keywords: ["INetFwAuthorizedApplication interface [ICS/ICF]","ProcessImageFileName property","INetFwAuthorizedApplication.ProcessImageFileName","INetFwAuthorizedApplication.get_ProcessImageFileName","INetFwAuthorizedApplication::ProcessImageFileName","INetFwAuthorizedApplication::get_ProcessImageFileName","INetFwAuthorizedApplication::put_ProcessImageFileName","ProcessImageFileName property [ICS/ICF]","ProcessImageFileName property [ICS/ICF]","INetFwAuthorizedApplication interface","get_ProcessImageFileName","ics.inetfwauthorizedapplication_processimagefilename","netfw/INetFwAuthorizedApplication::ProcessImageFileName","netfw/INetFwAuthorizedApplication::get_ProcessImageFileName","netfw/INetFwAuthorizedApplication::put_ProcessImageFileName"]
old-location: ics\inetfwauthorizedapplication_processimagefilename.htm
tech.root: ics
ms.assetid: 14e7c8e1-088c-4eae-8f93-7ee41bfa484b
ms.date: 12/05/2018
ms.keywords: INetFwAuthorizedApplication interface [ICS/ICF],ProcessImageFileName property, INetFwAuthorizedApplication.ProcessImageFileName, INetFwAuthorizedApplication.get_ProcessImageFileName, INetFwAuthorizedApplication::ProcessImageFileName, INetFwAuthorizedApplication::get_ProcessImageFileName, INetFwAuthorizedApplication::put_ProcessImageFileName, ProcessImageFileName property [ICS/ICF], ProcessImageFileName property [ICS/ICF],INetFwAuthorizedApplication interface, get_ProcessImageFileName, ics.inetfwauthorizedapplication_processimagefilename, netfw/INetFwAuthorizedApplication::ProcessImageFileName, netfw/INetFwAuthorizedApplication::get_ProcessImageFileName, netfw/INetFwAuthorizedApplication::put_ProcessImageFileName
req.header: netfw.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 with SP1 [desktop apps only]
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
req.dll: FirewallAPI.dll; Hnetcfg.dll on Windows XP with SP2
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - INetFwAuthorizedApplication::get_ProcessImageFileName
 - netfw/INetFwAuthorizedApplication::get_ProcessImageFileName
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - FirewallAPI.dll
 - Hnetcfg.dll
api_name:
 - INetFwAuthorizedApplication.ProcessImageFileName
 - INetFwAuthorizedApplication.get_ProcessImageFileName
 - INetFwAuthorizedApplication.put_ProcessImageFileName
---

# INetFwAuthorizedApplication::get_ProcessImageFileName


## -description

<p class="CCE_Message">[The Windows Firewall API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. For Windows Vista and later, use of the <a href="/previous-versions/windows/desktop/ics/windows-firewall-advanced-security-start-page">Windows Firewall with Advanced Security</a> API is recommended.]

Specifies the process image file name for this application.

This property is read/write.

## -parameters

## -remarks

The image file name must be a fully qualified path and reference an existing application.  The name may contain environment variables.

This property is required.

A demonstration of this property can be found in the VBScript code example <a href="/previous-versions/windows/desktop/ics/wf-adding-an-application">Adding an Application</a>.

## -see-also

<a href="/previous-versions/windows/desktop/ics/wf-adding-an-application">Adding an Application</a>



<a href="/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwauthorizedapplication">INetFwAuthorizedApplication</a>
