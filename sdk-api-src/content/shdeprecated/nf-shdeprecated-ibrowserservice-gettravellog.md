---
UID: NF:shdeprecated.IBrowserService.GetTravelLog
title: IBrowserService::GetTravelLog (shdeprecated.h)
description: Deprecated. Retrieves the browser's ITravelLog.
helpviewer_keywords: ["GetTravelLog","GetTravelLog method [Windows Shell]","GetTravelLog method [Windows Shell]","IBrowserService interface","IBrowserService interface [Windows Shell]","GetTravelLog method","IBrowserService.GetTravelLog","IBrowserService::GetTravelLog","shdeprecated/IBrowserService::GetTravelLog","shell.IBrowserService_GetTravelLog","zone_IBrowserService_GetTravelLog"]
old-location: shell\IBrowserService_GetTravelLog.htm
tech.root: shell
ms.assetid: 8e6c09e4-5489-4c21-8e42-28cdc4c216f1
ms.date: 12/05/2018
ms.keywords: GetTravelLog, GetTravelLog method [Windows Shell], GetTravelLog method [Windows Shell],IBrowserService interface, IBrowserService interface [Windows Shell],GetTravelLog method, IBrowserService.GetTravelLog, IBrowserService::GetTravelLog, shdeprecated/IBrowserService::GetTravelLog, shell.IBrowserService_GetTravelLog, zone_IBrowserService_GetTravelLog
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
req.product: Internet Explorer 4.0
ms.custom: 19H1
f1_keywords:
 - IBrowserService::GetTravelLog
 - shdeprecated/IBrowserService::GetTravelLog
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shdeprecated.h
api_name:
 - IBrowserService.GetTravelLog
---

# IBrowserService::GetTravelLog


## -description

Deprecated. Retrieves the browser's <a href="/windows/desktop/api/shdeprecated/nn-shdeprecated-itravellog">ITravelLog</a>.

## -parameters

### -param pptl [out]

Type: <b><a href="/windows/desktop/api/shdeprecated/nn-shdeprecated-itravellog">ITravelLog</a>**</b>

The address that receives a pointer to the browser's <a href="/windows/desktop/api/shdeprecated/nn-shdeprecated-itravellog">ITravelLog</a>.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.