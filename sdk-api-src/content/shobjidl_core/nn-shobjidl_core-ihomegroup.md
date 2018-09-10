---
UID: NN:shobjidl_core.IHomeGroup
title: IHomeGroup
author: windows-sdk-content
description: Exposes methods that determine a computer's HomeGroup membership status and display the sharing wizard.
old-location: shell\IHomeGroup.htm
tech.root: shell
ms.assetid: 97d693c0-1126-4cd3-8aee-b5499b538403
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: IHomeGroup, IHomeGroup interface [Windows Shell], IHomeGroup interface [Windows Shell],described, _shell_IHomeGroup, shell.IHomeGroup, shobjidl_core/IHomeGroup
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Provsvc.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Provsvc.dll
api_name:
 - IHomeGroup
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IHomeGroup interface


## -description


Exposes methods that determine a computer's HomeGroup membership status and display the sharing wizard.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IHomeGroup</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IHomeGroup</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IHomeGroup</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9ce98b11-46fd-4168-828d-a5ba8f71b7c9">IsMember</a>
</td>
<td align="left" width="63%">
Determines whether the local computer is a member of a HomeGroup.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/D73A97EE-B427-4c53-B023-3662D864E801">ShowSharingWizard</a>
</td>
<td align="left" width="63%">
Displays a wizard that allows a user to create a Home Group, and then retrieves the sharing options that the user selected through the wizard.

</td>
</tr>
</table> 


## -remarks



<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
Custom implementations of <b>IHomeGroup</b> are not supported; client applications use the implementation provided in Provsvc.dll.

<h3><a id="When_to_Use"></a><a id="when_to_use"></a><a id="WHEN_TO_USE"></a>When to Use</h3>
Use <b>IHomeGroup</b> when there is a need to determine the local computer's HomeGroup membership status; that is, to check wither the local computer is a member of a HomeGroup.



To create an instance of <b>IHomeGroup</b>, call <a href="https://msdn.microsoft.com/7295a55b-12c7-4ed0-a7a4-9ecee16afdec">CoCreateInstance</a> and specify <b>CLSID_HomeGroup</b> as the CLSID. <b>CLSID_HomeGroup</b> is defined in Shobjidl.h and Shobjidl.idl.



