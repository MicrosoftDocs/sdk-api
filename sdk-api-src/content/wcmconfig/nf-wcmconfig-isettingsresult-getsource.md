---
UID: NF:wcmconfig.ISettingsResult.GetSource
title: ISettingsResult::GetSource
author: windows-sdk-content
description: Returns the file or path where the error has occurred.
old-location: smi\isettingsresult_getsource.htm
tech.root: SMI
ms.assetid: 2a76b243-5294-47a7-8ad3-b39425735866
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetSource, GetSource method [SMI], GetSource method [SMI],ISettingsResult interface, ISettingsResult interface [SMI],GetSource method, ISettingsResult.GetSource, ISettingsResult::GetSource, smi.isettingsresult_getsource, wcmconfig/ISettingsResult::GetSource
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wcmconfig.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WcmConfig.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: SMIEngine.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - SMIEngine.dll
api_name:
 - ISettingsResult.GetSource
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- wcmconfig.h
: 
- ISettingsResult.GetSource
: 
---

# ISettingsResult::GetSource


## -description


Returns the file or path where the error has occurred.


## -parameters




### -param file [out]

The file or path where the error has occurred.


## -returns



This method returns an HRESULT value. <b>S_OK</b> indicates success. It may return <b>E_OUTOFMEMORY</b> if there are insufficient resources to return information to the user.




## -see-also




<a href="https://msdn.microsoft.com/0bbfd39a-0292-4d8e-ae31-f45aebd326a7">ISettingsResult</a>
 

 

