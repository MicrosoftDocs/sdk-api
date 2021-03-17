---
UID: NF:wuapi.IInstallationAgent.RecordInstallationResult
title: IInstallationAgent::RecordInstallationResult (wuapi.h)
description: Records the result for an update. The result is specified by an IStringCollection object.
helpviewer_keywords: ["IInstallationAgent interface [Windows Update Agent]","RecordInstallationResult method","IInstallationAgent.RecordInstallationResult","IInstallationAgent::RecordInstallationResult","RecordInstallationResult","RecordInstallationResult method [Windows Update Agent]","RecordInstallationResult method [Windows Update Agent]","IInstallationAgent interface","wua.iinstallationagent_recordinstallationresult","wuapi/IInstallationAgent::RecordInstallationResult"]
old-location: wua\iinstallationagent_recordinstallationresult.htm
tech.root: wua
ms.assetid: E2DD54E3-741E-4647-9993-A9476279BD6C
ms.date: 12/05/2018
ms.keywords: IInstallationAgent interface [Windows Update Agent],RecordInstallationResult method, IInstallationAgent.RecordInstallationResult, IInstallationAgent::RecordInstallationResult, RecordInstallationResult, RecordInstallationResult method [Windows Update Agent], RecordInstallationResult method [Windows Update Agent],IInstallationAgent interface, wua.iinstallationagent_recordinstallationresult, wuapi/IInstallationAgent::RecordInstallationResult
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IInstallationAgent::RecordInstallationResult
 - wuapi/IInstallationAgent::RecordInstallationResult
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wuapi.dll
api_name:
 - IInstallationAgent.RecordInstallationResult
---

# IInstallationAgent::RecordInstallationResult


## -description

Records the result for an update. The result is specified by an <a href="/windows/desktop/api/wuapi/nn-wuapi-istringcollection">IStringCollection</a> object.

## -parameters

### -param installationResultCookie [in]

A string value that identifies the result cookie.

### -param hresult [in]

The identifier of the result.

### -param extendedReportingData [in]

An <a href="/windows/desktop/api/wuapi/nn-wuapi-istringcollection">IStringCollection</a> interface that represents a collection of strings that contain the result for an update.

## -returns

Returns <b>S_OK</b> if successful. Otherwise, returns a COM or Windows error code.

## -see-also

<a href="/windows/desktop/api/wuapi/nn-wuapi-iinstallationagent">IInstallationAgent</a>