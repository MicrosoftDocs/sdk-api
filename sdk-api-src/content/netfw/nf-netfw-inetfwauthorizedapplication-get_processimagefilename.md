---
UID: NF:netfw.INetFwAuthorizedApplication.get_ProcessImageFileName
title: INetFwAuthorizedApplication::get_ProcessImageFileName
author: windows-sdk-content
description: Specifies the process image file name for this application.
old-location: ics\inetfwauthorizedapplication_processimagefilename.htm
old-project: ICS
ms.assetid: 14e7c8e1-088c-4eae-8f93-7ee41bfa484b
ms.author: windowssdkdev
ms.date: 05/11/2018
ms.keywords: INetFwAuthorizedApplication interface [ICS/ICF],ProcessImageFileName property, INetFwAuthorizedApplication.ProcessImageFileName, INetFwAuthorizedApplication.get_ProcessImageFileName, INetFwAuthorizedApplication::ProcessImageFileName, INetFwAuthorizedApplication::get_ProcessImageFileName, INetFwAuthorizedApplication::put_ProcessImageFileName, ProcessImageFileName property [ICS/ICF], ProcessImageFileName property [ICS/ICF],INetFwAuthorizedApplication interface, get_ProcessImageFileName, ics.inetfwauthorizedapplication_processimagefilename, netfw/INetFwAuthorizedApplication::ProcessImageFileName, netfw/INetFwAuthorizedApplication::get_ProcessImageFileName, netfw/INetFwAuthorizedApplication::put_ProcessImageFileName
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: NETISO_ERROR_TYPE
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
product: Windows
targetos: Windows
req.lib: 
req.dll: FirewallAPI.dll; Hnetcfg.dll on Windows XP with SP2
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# INetFwAuthorizedApplication::get_ProcessImageFileName


## -description


<p class="CCE_Message">[The Windows Firewall API is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. For Windows Vista and later, use of the <a href="https://msdn.microsoft.com/8F33B96B-AA9A-46d5-8808-0F2D0723935B">Windows Firewall with Advanced Security</a> API is recommended.]

Specifies the process image file name for this application.

This property is read/write.


## -parameters


## -remarks



The image file name must be a fully qualified path and reference an existing application.  The name may contain environment variables.

This property is required.

A demonstration of this property can be found in the VBScript code example <a href="https://msdn.microsoft.com/47a09bbc-7b34-41e4-bef8-124b275da0ba">Adding an Application</a>.




## -see-also




<a href="https://msdn.microsoft.com/47a09bbc-7b34-41e4-bef8-124b275da0ba">Adding an Application</a>



<a href="https://msdn.microsoft.com/1ddeeab8-b81b-4d34-9ca6-103147fb3426">INetFwAuthorizedApplication</a>
 

 

