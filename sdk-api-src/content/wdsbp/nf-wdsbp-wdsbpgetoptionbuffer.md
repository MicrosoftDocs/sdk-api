---
UID: NF:wdsbp.WdsBpGetOptionBuffer
title: WdsBpGetOptionBuffer function (wdsbp.h)
description: Copies information into a buffer that should be added to your DHCP packet options.
helpviewer_keywords: ["WdsBpGetOptionBuffer","WdsBpGetOptionBuffer function [Windows Deployment Services]","wds.wdsbpgetoptionbuffer","wdsbp/WdsBpGetOptionBuffer"]
old-location: wds\wdsbpgetoptionbuffer.htm
tech.root: wds
ms.assetid: 2bd4105d-0066-4c6b-a1c0-fe9b633a6ad6
ms.date: 12/05/2018
ms.keywords: WdsBpGetOptionBuffer, WdsBpGetOptionBuffer function [Windows Deployment Services], wds.wdsbpgetoptionbuffer, wdsbp/WdsBpGetOptionBuffer
req.header: wdsbp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista with SP1 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wdsbp.lib
req.dll: Wdsbp.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WdsBpGetOptionBuffer
 - wdsbp/WdsBpGetOptionBuffer
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wdsbp.dll
api_name:
 - WdsBpGetOptionBuffer
---

# WdsBpGetOptionBuffer function


## -description

Copies information into a buffer that should be added to your DHCP packet options.

## -parameters

### -param hHandle [in]

A handle to the packet. This handle must have been returned by the <a href="/windows/desktop/api/wdsbp/nf-wdsbp-wdsbpinitialize">WdsBpInitialize</a> function.

### -param uBufferLen [in]

The total number of bytes of memory pointed to by the <i>pBuffer</i> parameter.  To determine the amount of memory required, call the <b>WdsBpGetOptionBuffer</b> function with <i>uBufferLen</i> set to zero and  <i>pBuffer</i> set to <b>NULL</b>. The location pointed to by  the <i>puBytes</i> parameter then receives the size required.

### -param pBuffer [out]

A pointer to a location in memory that receives the information that is being sent to the network boot program.

### -param puBytes [out]

The number of bytes copied to the buffer.

## -returns

If the function succeeds, the return is <b>S_OK</b>.