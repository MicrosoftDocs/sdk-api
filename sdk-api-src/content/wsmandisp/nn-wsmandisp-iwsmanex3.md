---
UID: NN:wsmandisp.IWSManEx3
title: IWSManEx3
author: windows-sdk-content
description: Extends the methods and properties of the IWSManEx interface to include a method that returns a session flag value related to authentication using the Credential Security Support Provider (CredSSP).
old-location: winrm\iwsmanex3.htm
tech.root: winrm
ms.assetid: 6d362cdf-0f77-446a-8df9-1d38eca853a2
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWSManEx3, IWSManEx3 interface [Windows Remote Management], IWSManEx3 interface [Windows Remote Management],described, winrm.iwsmanex3, wsmandisp/IWSManEx3
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: wsmandisp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7
req.target-min-winversvr: Windows Server 2008 R2
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WSManDisp.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: WSManDisp.tlb
req.dll: WSMAuto.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - WSMAuto.dll
api_name:
 - IWSManEx3
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Management Framework on Windows Server 2008 with SP2 and Windows Vista with SP2
---

# IWSManEx3 interface


## -description


Extends the methods and properties of the <a href="https://msdn.microsoft.com/23fdd9d9-4a78-4c01-8e5d-c8007f39d5d6">IWSManEx</a> interface to include a method that returns a session flag value related to authentication using the Credential Security Support Provider (CredSSP).


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWSManEx3</b> interface inherits from <a href="https://msdn.microsoft.com/23fdd9d9-4a78-4c01-8e5d-c8007f39d5d6">IWSManEx</a>. <b>IWSManEx3</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWSManEx3</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/69c62ad1-319e-4716-a2c7-61b931567244">IWSManEx3::SessionFlagUseCredSsp</a>
</td>
<td align="left" width="63%">
Returns the value of the authentication flag <b>WSManFlagUseCredSsp</b>.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/23fdd9d9-4a78-4c01-8e5d-c8007f39d5d6">IWSManEx</a>
 

 

