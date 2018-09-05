---
UID: NN:wsbapp.IWsbApplicationBackupSupport
title: IWsbApplicationBackupSupport
author: windows-sdk-content
description: Defines a method for checking the consistency of the application's VSS writer's components.
old-location: wsb\iwsbapplicationbackupsupport.htm
old-project: wsb
ms.assetid: 45865f1b-0f0a-46fc-b1f3-f2fd7c49f56f
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IWsbApplicationBackupSupport, IWsbApplicationBackupSupport interface [Windows Server Backup], IWsbApplicationBackupSupport interface [Windows Server Backup],described, wsb.iwsbapplicationbackupsupport, wsbapp/IWsbApplicationBackupSupport
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: wsbapp.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WsbApp.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WSPUPCALLTABLE, *LPWSPUPCALLTABLE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - WsbApp.h
api_name:
 - IWsbApplicationBackupSupport
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWsbApplicationBackupSupport interface


## -description


Defines a method for checking the consistency of the application's VSS writer's components.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWsbApplicationBackupSupport</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWsbApplicationBackupSupport</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWsbApplicationBackupSupport</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/27ec1ee5-d612-48eb-8a5b-41e01c7f28d3">CheckConsistency</a>
</td>
<td align="left" width="63%">
Checks the consistency of the VSS writer's components in the shadow copy after shadow copies are created for the volumes to be backed up.

</td>
</tr>
</table> 

