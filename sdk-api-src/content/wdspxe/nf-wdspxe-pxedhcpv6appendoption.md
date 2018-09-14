---
UID: NF:wdspxe.PxeDhcpv6AppendOption
title: PxeDhcpv6AppendOption function
author: windows-sdk-content
description: Appends a DHCPv6 option to the reply packet.
old-location: wds\pxedhcpv6appendoption.htm
tech.root: wds
ms.assetid: 92A35846-360B-42D3-935B-6FC10AF687A5
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: PxeDhcpv6AppendOption, PxeDhcpv6AppendOption function [Windows Deployment Services], wds.pxedhcpv6appendoption, wdspxe/PxeDhcpv6AppendOption
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wdspxe.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: WdsPxe.lib
req.dll: WdsPxe.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - WdsPxe.dll
api_name:
 - PxeDhcpv6AppendOption
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PxeDhcpv6AppendOption function


## -description


Appends a DHCPv6 option to the reply packet.


## -parameters




### -param pReply [in, out]

Pointer to a reply packet allocated with the 
      <a href="https://msdn.microsoft.com/f3a664a8-565c-4894-bea7-6664df0ecd9b">PxePacketAllocate</a> function.


### -param cbReply [in]

The total size in bytes allocated for the buffer that is pointed to by <i>pReply</i>.


### -param pcbReplyUsed [in, out]

On entry, this is the number of bytes of the buffer pointed to by <i>pReply</i> that are currently used.  On success of the function, this is updated to the number of bytes used after appending the option.


### -param wOptionType [in]

DHCPv6 option to add to the packet.


### -param cbOption [in]

Length of the option value pointed to by the <i>pOption</i> parameter. 


### -param pOption [in]

Address of the buffer that contains the DHCPv6 option value.


## -returns



If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.




## -see-also




<a href="https://msdn.microsoft.com/f3a664a8-565c-4894-bea7-6664df0ecd9b">PxePacketAllocate</a>



<a href="https://msdn.microsoft.com/b6089ff9-4d74-4f5d-957f-4a741c09f4b9">Windows Deployment Services Server Functions</a>
 

 

