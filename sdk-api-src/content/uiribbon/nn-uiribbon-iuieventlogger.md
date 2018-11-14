---
UID: NN:uiribbon.IUIEventLogger
title: IUIEventLogger
author: windows-sdk-content
description: The IUIEventLogger interface is implemented by the application and defines the ribbon events callback method.
old-location: windowsribbon\iuieventlogger.htm
tech.root: windowsribbon
ms.assetid: 54DB1BFF-0657-4027-8C8C-89CE998253F4
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IUIEventLogger, IUIEventLogger interface [Windows Ribbon], IUIEventLogger interface [Windows Ribbon],described, uiribbon/IUIEventLogger, windowsribbon.iuieventlogger
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: uiribbon.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Uiribbon.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Uiribbon.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Uiribbon.dll
api_name:
 - IUIEventLogger
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIEventLogger interface


## -description


The <b>IUIEventLogger</b> interface is implemented by the 
				application and defines the ribbon events callback method.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUIEventLogger</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IUIEventLogger</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IUIEventLogger</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1BE6F914-C57D-4A8F-A286-C47BFD48B310">OnUIEvent</a>
</td>
<td align="left" width="63%">
Receives notifications that a ribbon event has occurred.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/11E53D75-B8C0-40A3-8E4D-ACAA10BEAC84">IUIEventingManager</a>



<a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd371356(v=VS.85).aspx">Interfaces</a>
 

 

