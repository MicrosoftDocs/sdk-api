---
UID: NF:wdspxe.PxeDhcpAppendOptionRaw
title: PxeDhcpAppendOptionRaw function
author: windows-driver-content
description: Appends a DHCP option to the reply packet.
old-location: wds\pxedhcpappendoptionraw.htm
old-project: Wds
ms.assetid: f6525a06-a3b0-4989-8132-fa8f1ad2fec3
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: PxeDhcpAppendOption, PxeDhcpAppendOption function [Windows Deployment Services], PxeDhcpAppendOptionRaw, wds.pxedhcpappendoptionraw, wdspxe/PxeDhcpAppendOption
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wdspxe.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008, Windows Server 2003 with SP2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WDS_CLI_CRED, *PWDS_CLI_CRED, *LPWDS_CLI_CRED
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	WdsPxe.dll
api_name:
-	PxeDhcpAppendOption
product: Windows
targetos: Windows
req.lib: WdsPxe.lib
req.dll: WdsPxe.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# PxeDhcpAppendOptionRaw function


## -description


Appends a DHCP option to the reply packet.


## -parameters




### -param pReplyPacket [in, out]

Pointer to a reply packet allocated with the 
      <a href="https://msdn.microsoft.com/f3a664a8-565c-4894-bea7-6664df0ecd9b">PxePacketAllocate</a> function.


### -param uMaxReplyPacketLen [in]

Allocated length of the packet pointed to by the <i>pReplyPacket</i> parameter.


### -param puReplyPacketLen [in, out]

Address of a <b>ULONG</b> that on successful completion will receive the length of 
      the packet pointed to by the <i>pReplyPacket</i> parameter.


### -param uBufferLen [in]

Length of the option value pointed to by the <i>pBuffer</i> parameter. 


### -param pBuffer [in]

Address of the buffer that contains the DHCP option value. 


## -returns



If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.




## -see-also




<a href="https://msdn.microsoft.com/f3a664a8-565c-4894-bea7-6664df0ecd9b">PxePacketAllocate</a>



<a href="https://msdn.microsoft.com/b6089ff9-4d74-4f5d-957f-4a741c09f4b9">Windows Deployment Services Server Functions</a>
 

 

