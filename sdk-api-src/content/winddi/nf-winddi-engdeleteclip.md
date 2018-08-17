---
UID: NF:winddi.EngDeleteClip
title: EngDeleteClip function
author: windows-sdk-content
description: The EngDeleteClip function deletes a CLIPOBJ structure allocated by EngCreateClip.
old-location: display\engdeleteclip.htm
old-project: display
ms.assetid: 7af85df1-1e37-4a69-82a0-1c1eec32dd48
ms.author: windowssdkdev
ms.date: 08/13/2018
ms.keywords: EngDeleteClip, EngDeleteClip function [Display Devices], display.engdeleteclip, gdifncs_0ca10e14-e720-49f3-8c56-9c9dd646f04f.xml, winddi/EngDeleteClip
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winddi.h
req.include-header: Winddi.h
req.redist: 
req.target-type: Universal
req.target-min-winverclnt: Available in Windows 2000 and later versions of the Windows operating systems.
req.target-min-winversvr: 
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
req.typenames: SSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS, *PSSL_F12_EXTRA_CERT_CHAIN_POLICY_STATUS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Win32k.sys
api_name:
 - EngDeleteClip
product: Windows
targetos: Windows
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
req.product: Windows Address Book 5.0
---

# EngDeleteClip function


## -description


The <b>EngDeleteClip</b> function deletes a <a href="https://msdn.microsoft.com/c3f632ed-f8d1-44bb-b2fb-6f7f2c71fd63">CLIPOBJ</a> structure allocated by <a href="https://msdn.microsoft.com/719b006f-1eb0-41c6-8b88-c8241a394abe">EngCreateClip</a>.


## -parameters




### -param pco

Pointer to the CLIPOBJ structure to delete.


## -returns



None



