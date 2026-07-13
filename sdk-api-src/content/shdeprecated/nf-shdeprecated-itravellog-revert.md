---
UID: NF:shdeprecated.ITravelLog.Revert
title: ITravelLog::Revert (shdeprecated.h)
description: Deprecated. Reverts to the current entry, dropping the result of ITravelLog::AddEntry in the case of a failed navigation.
helpviewer_keywords: ["ITravelLog interface [Windows Shell]","Revert method","ITravelLog.Revert","ITravelLog::Revert","Revert","Revert method [Windows Shell]","Revert method [Windows Shell]","ITravelLog interface","shdeprecated/ITravelLog::Revert","shell.ITravelLog_Revert","zone_ITravelLog_Revert"]
old-location: shell\ITravelLog_Revert.htm
tech.root: shell
ms.assetid: 202ce028-d64c-4733-8006-1bdb1efa8ad3
ms.date: 12/05/2018
ms.keywords: ITravelLog interface [Windows Shell],Revert method, ITravelLog.Revert, ITravelLog::Revert, Revert, Revert method [Windows Shell], Revert method [Windows Shell],ITravelLog interface, shdeprecated/ITravelLog::Revert, shell.ITravelLog_Revert, zone_ITravelLog_Revert
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
 - ITravelLog::Revert
 - shdeprecated/ITravelLog::Revert
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
 - ITravelLog.Revert
---

# ITravelLog::Revert


## -description

Deprecated. Reverts to the current entry, dropping the result of <a href="/windows/desktop/api/shdeprecated/nf-shdeprecated-itravellog-addentry">ITravelLog::AddEntry</a> in the case of a failed navigation.



## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.
