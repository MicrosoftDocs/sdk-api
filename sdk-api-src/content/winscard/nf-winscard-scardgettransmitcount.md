---
UID: NF:winscard.SCardGetTransmitCount
title: SCardGetTransmitCount function
author: windows-sdk-content
description: Retrieves the number of transmit operations that have completed since the specified card reader was inserted.
old-location: security\scardgettransmitcount.htm
old-project: SecAuthN
ms.assetid: 13857fc3-374d-4ba5-b4ca-e523b323974c
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: SCardGetTransmitCount, SCardGetTransmitCount function [Security], security.scardgettransmitcount, winscard/SCardGetTransmitCount
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: WINSAT_BITMAP_SIZE
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
req.lib: Winscard.lib
req.dll: Winscard.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
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

If the function fails, it returns an error code. For more information, see <a href="authentication_return_values.htm">Smart Card Return Values</a>.



