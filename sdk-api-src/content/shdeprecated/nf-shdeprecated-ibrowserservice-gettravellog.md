---
UID: NF:shdeprecated.IBrowserService.GetTravelLog
title: IBrowserService::GetTravelLog
author: windows-sdk-content
description: Deprecated. Retrieves the browser's ITravelLog.
old-location: shell\IBrowserService_GetTravelLog.htm
old-project: shell
ms.assetid: 8e6c09e4-5489-4c21-8e42-28cdc4c216f1
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: GetTravelLog, GetTravelLog method [Windows Shell], GetTravelLog method [Windows Shell],IBrowserService interface, IBrowserService interface [Windows Shell],GetTravelLog method, IBrowserService.GetTravelLog, IBrowserService::GetTravelLog, shdeprecated/IBrowserService::GetTravelLog, shell.IBrowserService_GetTravelLog, zone_IBrowserService_GetTravelLog
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: shdeprecated.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shdeprecated.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: BNSTATE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shdeprecated.h
api_name:
 - IBrowserService.GetTravelLog
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 4.0
---

# IBrowserService::GetTravelLog


## -description


Deprecated. Retrieves the browser's <a href="https://msdn.microsoft.com/820869aa-ca93-4bb5-831a-3afb52da5389">ITravelLog</a>.


## -parameters




### -param pptl [out]

Type: <b><a href="https://msdn.microsoft.com/820869aa-ca93-4bb5-831a-3afb52da5389">ITravelLog</a>**</b>


          The address that receives a pointer to the browser's <a href="https://msdn.microsoft.com/820869aa-ca93-4bb5-831a-3afb52da5389">ITravelLog</a>.
        


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



