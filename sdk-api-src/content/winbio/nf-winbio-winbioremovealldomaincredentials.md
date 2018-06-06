---
UID: NF:winbio.WinBioRemoveAllDomainCredentials
title: WinBioRemoveAllDomainCredentials function
author: windows-sdk-content
description: Removes all user credentials for the current domain from the store. Starting with Windows 10, build 1607, this function is available to use with a mobile image.
old-location: secbiomet\winbioremovealldomaincredentials.htm
old-project: SecBioMet
ms.assetid: 2aee0929-2340-4901-a5d2-f1cd4395624a
ms.author: windowssdkdev
ms.date: 04/24/2018
ms.keywords: WinBioRemoveAllDomainCredentials, WinBioRemoveAllDomainCredentials function [Windows Biometric Framework API], secbiomet.winbioremovealldomaincredentials, winbio/WinBioRemoveAllDomainCredentials
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winbio.h
req.include-header: Winbio.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: WINBIO_ASYNC_NOTIFICATION_METHOD, *PWINBIO_ASYNC_NOTIFICATION_METHOD
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Winbio.dll
 - ext-ms-win-biometrics-winbio-core-l1-1-0.dll
 - Ext-MS-Win-BioMetrics-WinBio-Core-L1-1-1.dll
api_name:
 - WinBioRemoveAllDomainCredentials
product: Windows
targetos: Windows
req.lib: Winbio.lib
req.dll: Winbio.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# WinBioRemoveAllDomainCredentials function


## -description


Removes all user credentials for the current domain from the store. Starting with Windows 10, build 1607, this  function is available to use with a mobile image.


## -parameters






## -returns



If the function succeeds, it returns S_OK. If the function fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -see-also




<a href="https://msdn.microsoft.com/3c3f3bed-531a-4962-8eb3-bebe16bed3a8">WinBioRemoveAllCredentials</a>



<a href="https://msdn.microsoft.com/56a5d510-f2cb-457b-884a-ad08ea21ce01">WinBioRemoveCredential</a>



<a href="https://msdn.microsoft.com/c35dd874-c545-418a-b08c-82f9e13e93fb">WinBioSetCredential</a>
 

 

