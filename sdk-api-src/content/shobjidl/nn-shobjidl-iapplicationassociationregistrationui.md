---
UID: NN:shobjidl.IApplicationAssociationRegistrationUI
title: IApplicationAssociationRegistrationUI
author: windows-driver-content
description: Exposes a method that launches an advanced association dialog box through which the user can customize their associations.
old-location: shell\IApplicationAssociationRegistrationUI.htm
old-project: shell
ms.assetid: 3a4d6f1d-72c2-4bd0-ad44-1c42a5bf9cb6
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: IApplicationAssociationRegistrationUI, IApplicationAssociationRegistrationUI interface [Windows Shell], IApplicationAssociationRegistrationUI interface [Windows Shell],described, _shell_IApplicationAssociationRegistrationUI, shell.IApplicationAssociationRegistrationUI, shobjidl/IApplicationAssociationRegistrationUI
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: shobjidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: VPWATERMARKFLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Shobjidl.h
api_name:
-	IApplicationAssociationRegistrationUI
product: Windows
targetos: Windows
req.lib: Shell32.lib
req.dll: Shell32.dll
req.irql: 
req.product: Internet Explorer 6.01
---

# IApplicationAssociationRegistrationUI interface


## -description


Exposes a method that launches an advanced association dialog box through which the user can customize their associations.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IApplicationAssociationRegistrationUI</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IApplicationAssociationRegistrationUI</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IApplicationAssociationRegistrationUI</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/db2fc087-2f22-40df-8ec9-f673c0fe81ff">LaunchAdvancedAssociationUI</a>
</td>
<td align="left" width="63%">
Launches an advanced association dialog box through which the user can customize the associations for the application specified in <i>pszAppRegName</i>.

</td>
</tr>
</table> 


## -remarks



Because <b>IApplicationAssociationRegistrationUI</b> is only supported for Windows Vista and later, applications that support earlier operating systems must use their preexisting code when running under those operating systems. Those applications should include a check for the operating system version to account for this.




## -see-also




<a href="https://msdn.microsoft.com/78cd05a4-df33-42b5-91b9-826ebce04a1d">Default Programs</a>
 

 

