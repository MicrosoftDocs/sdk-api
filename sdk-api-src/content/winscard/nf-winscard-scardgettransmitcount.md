---
UID: NF:winscard.SCardGetTransmitCount
title: SCardGetTransmitCount function
author: windows-sdk-content
description: Retrieves the number of transmit operations that have completed since the specified card reader was inserted.
old-location: security\scardgettransmitcount.htm
tech.root: secauthn
ms.assetid: 13857fc3-374d-4ba5-b4ca-e523b323974c
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: SCardGetTransmitCount, SCardGetTransmitCount function [Security], security.scardgettransmitcount, winscard/SCardGetTransmitCount
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winscard.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
req.lib: Winscard.lib
req.dll: Winscard.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Winscard.dll
api_name:
 - SCardGetTransmitCount
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SCardGetTransmitCount function


## -description


The <b>SCardGetTransmitCount</b> function retrieves the number of transmit operations that have completed since the specified card reader was inserted.


## -parameters




### -param hCard [in]

A handle to a smart card obtained from a previous call to 
<a href="https://msdn.microsoft.com/389ada98-383f-4b37-bf5d-c40577ef25fd">SCardConnect</a>.


### -param pcTransmitCount [out]

A pointer to the number of transmit operations that have completed since the specified card reader was inserted.


## -returns



If the function succeeds, it returns <b>SCARD_S_SUCCESS</b>. 

If the function fails, it returns an error code. For more information, see <a href="https://msdn.microsoft.com/en-us/library/Aa374738(v=VS.85).aspx">Smart Card Return Values</a>.



