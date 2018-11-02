---
UID: NF:wdsbp.WdsBpGetOptionBuffer
title: WdsBpGetOptionBuffer function
author: windows-sdk-content
description: Copies information into a buffer that should be added to your DHCP packet options.
old-location: wds\wdsbpgetoptionbuffer.htm
tech.root: wds
ms.assetid: 2bd4105d-0066-4c6b-a1c0-fe9b633a6ad6
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: WdsBpGetOptionBuffer, WdsBpGetOptionBuffer function [Windows Deployment Services], wds.wdsbpgetoptionbuffer, wdsbp/WdsBpGetOptionBuffer
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wdsbp.dll
api_name:
 - WdsBpGetOptionBuffer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WdsBpGetOptionBuffer function


## -description


Copies information into a buffer that should be added to your DHCP packet options.


## -parameters




### -param hHandle [in]

A handle to the packet. This handle must have been returned by the <a href="https://msdn.microsoft.com/a77cbdf5-9025-4e98-8edd-1b9bae8493e7">WdsBpInitialize</a> function.


### -param uBufferLen [in]

The total number of bytes of memory pointed to by the <i>pBuffer</i> parameter.  To determine the amount of memory required, call the <b>WdsBpGetOptionBuffer</b> function with <i>uBufferLen</i> set to zero and  <i>pBuffer</i> set to <b>NULL</b>. The location pointed to by  the <i>puBytes</i> parameter then receives the size required.


### -param pBuffer [out]

A pointer to a location in memory that receives the information that is being sent to the network boot program.


### -param puBytes [out]

The number of bytes copied to the buffer. 


## -returns



If the function succeeds, the return is <b>S_OK</b>.



