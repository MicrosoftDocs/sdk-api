---
UID: NN:isolatedapplauncher.IIsolatedAppLauncher
title: IIsolatedAppLauncher
author: windows-driver-content
description: Enables apps to determine whether they are running in a Windows Defender Application Guard container (VM container environment).
old-location: winprog\iisolatedapplauncher.htm
old-project: DevNotes
ms.assetid: 49C30C52-ACE7-446D-A9B2-5BA7C6583700
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: IIsolatedAppLauncher, IIsolatedAppLauncher interface [Windows API], IIsolatedAppLauncher interface [Windows API],described, isolatedapplauncher/IIsolatedAppLauncher, winprog.iisolatedapplauncher
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: isolatedapplauncher.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
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
req.typenames: ISCSI_UNIQUE_SESSION_ID, *PISCSI_UNIQUE_SESSION_ID, ISCSI_UNIQUE_CONNECTION_ID, *PISCSI_UNIQUE_CONNECTION_ID
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	isolatedapplauncher.h
api_name:
-	IIsolatedAppLauncher
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IIsolatedAppLauncher interface


## -description


Enables apps to determine whether they are running in a Windows Defender Application Guard container (VM container environment). 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IIsolatedAppLauncher</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IIsolatedAppLauncher</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IIsolatedAppLauncher</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/C7883F93-FE00-4515-928E-0778FB5324C3">IsProcessInIsolatedContainer</a>
</td>
<td align="left" width="63%">
Indicates whether the current execution environment is a Windows Defender Application Guard container (VM container environment).

</td>
</tr>
</table> 

