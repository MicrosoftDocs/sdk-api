---
UID: NF:wuapi.IInstallationAgent.RecordInstallationResult
title: IInstallationAgent::RecordInstallationResult
author: windows-sdk-content
description: Records the result for an update. The result is specified by an IStringCollection object.
old-location: wua\iinstallationagent_recordinstallationresult.htm
tech.root: wua_sdk
ms.assetid: E2DD54E3-741E-4647-9993-A9476279BD6C
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IInstallationAgent interface [Windows Update Agent],RecordInstallationResult method, IInstallationAgent.RecordInstallationResult, IInstallationAgent::RecordInstallationResult, RecordInstallationResult, RecordInstallationResult method [Windows Update Agent], RecordInstallationResult method [Windows Update Agent],IInstallationAgent interface, wua.iinstallationagent_recordinstallationresult, wuapi/IInstallationAgent::RecordInstallationResult
ms.topic: method
req.header: wuapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional with SP3 [desktop apps only]
req.target-min-winversvr: Windows Server 2003, Windows 2000 Server with SP3 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wuapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wuguid.lib
req.dll: Wuapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wuapi.dll
api_name:
 - IInstallationAgent.RecordInstallationResult
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IInstallationAgent::RecordInstallationResult


## -description


Records the result for an update. The result is specified by an <a href="https://msdn.microsoft.com/3aaab669-1f80-41ee-8c29-6da613ebccff">IStringCollection</a> object.


## -parameters




### -param installationResultCookie [in]

A string value that identifies the result cookie.


### -param hresult [in]

The identifier of the result.


### -param extendedReportingData [in]

An <a href="https://msdn.microsoft.com/3aaab669-1f80-41ee-8c29-6da613ebccff">IStringCollection</a> interface that represents a collection of strings that contain the result for an update.


## -returns



Returns <b>S_OK</b> if successful. Otherwise, returns a COM or Windows error code. 




## -see-also




<a href="https://msdn.microsoft.com/B24B527C-D92B-4BEB-ADCC-5E2BA684A478">IInstallationAgent</a>
 

 

