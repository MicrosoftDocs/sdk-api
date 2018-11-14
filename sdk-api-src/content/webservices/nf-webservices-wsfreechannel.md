---
UID: NF:webservices.WsFreeChannel
title: WsFreeChannel function
author: windows-sdk-content
description: Releases the memory resource associated with a Channel object.
old-location: wsw\wsfreechannel.htm
tech.root: wsw
ms.assetid: 74e36d19-c6db-4bba-90e3-88a48b6a1fb5
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: WsFreeChannel, WsFreeChannel function [Web Services for Windows], webservices/WsFreeChannel, wsw.wsfreechannel
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: webservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: WebServices.lib
req.dll: WebServices.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - WebServices.dll
api_name:
 - WsFreeChannel
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- WsFreeChannel
: 
---

# WsFreeChannel function


## -description


Releases the memory resource associated with a Channel object.
            
                The <b>Channel</b> must be in the either the <a href="https://msdn.microsoft.com/3a7f5bbd-e484-4a7e-8e5d-df229a7227a5">WS_CHANNEL_STATE_CREATED</a> 
                or <b>WS_CHANNEL_STATE_CLOSED</b> state to be released.
            If a Channel has been successfully opened it must be closed before it
                can be released.
            


## -parameters




### -param channel [in]

A pointer to the <b>Channel</b> object to release. The pointer must reference a valid <a href="https://msdn.microsoft.com/741636a4-5e0f-495a-bb1d-1a00cfd6f65a">WS_CHANNEL</a> object returned
                    by <a href="https://msdn.microsoft.com/4bef6f97-06f1-442a-8b84-869776f0541d">WsCreateChannel</a> or <a href="https://msdn.microsoft.com/d9a80506-d891-4cfd-b120-0d3fce946cf5">WsCreateChannelForListener</a>.
                    The referenced value may not be <b>NULL</b>.


## -returns



This function does not return a value.




## -remarks



A channel that is in the process of being accepted/opened cannot be
                released until the accept/open completes.  Use <a href="https://msdn.microsoft.com/67af85d7-db75-4e26-a7cc-8115ac3f2d59">WsAbortChannel</a> to cancel the accept/open process.
            



