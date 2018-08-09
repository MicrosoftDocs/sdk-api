---
UID: NN:shobjidl_core.IApplicationAssociationRegistration
title: IApplicationAssociationRegistration
author: windows-sdk-content
description: Exposes methods that query and set default applications for specific file Association Type, and protocols at a specific Association Level.
old-location: shell\IApplicationAssociationRegistration.htm
old-project: shell
ms.assetid: 015a3be4-2e74-4a2b-8c02-54dcbf0ecacd
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IApplicationAssociationRegistration, IApplicationAssociationRegistration interface [Windows Shell], IApplicationAssociationRegistration interface [Windows Shell],described, _shell_IApplicationAssociationRegistration, shell.IApplicationAssociationRegistration, shobjidl_core/IApplicationAssociationRegistration
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IApplicationAssociationRegistration
product: Windows
targetos: Windows
req.lib: Shell32.lib
req.dll: Browseui.dll
req.irql: 
req.product: Outlook Express 6.0
---

# IApplicationAssociationRegistration interface


## -description


Exposes methods that query and set default applications for specific file <a href="https://msdn.microsoft.com/3dbbe748-5e83-4103-932a-b51a2a55f9fd">Association Type</a>, and protocols at a specific <a href="https://msdn.microsoft.com/846ce9f4-092a-420d-be73-0951efc4368f">Association Level</a>.

            
<div class="alert"><b>Note</b>  As of Windows 8, the only functionality of this interface that is supported is <a href="https://msdn.microsoft.com/af6bd032-1457-4805-9844-87b5efb5ba21">QueryCurrentDefault</a>.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IApplicationAssociationRegistration</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IApplicationAssociationRegistration</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IApplicationAssociationRegistration</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dcc0990a-f678-47bb-9462-905940ac87d6">ClearUserAssociations</a>
</td>
<td align="left" width="63%">
Removes all per-user associations for the current user. This results in a reversion to machine defaults, if they exist.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/63127fa4-be09-4dd6-9084-cfde00967279">QueryAppIsDefault</a>
</td>
<td align="left" width="63%">
Determines whether an application owns the registered default association for a given application level and type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/71073f30-51bc-4522-9bb2-7eb743bca159">QueryAppIsDefaultAll</a>
</td>
<td align="left" width="63%">
Determines whether an application owns all of the registered default associations for a given application level.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/af6bd032-1457-4805-9844-87b5efb5ba21">QueryCurrentDefault</a>
</td>
<td align="left" width="63%">
Determines the default application for a given association type. This is the default application launched by <a href="https://msdn.microsoft.com/8b1f3978-a0ee-4684-8a37-98e270b63897">ShellExecute</a> for that type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/30870adb-793f-404f-809c-1ec34a1f6b82">SetAppAsDefault</a>
</td>
<td align="left" width="63%">
Sets an application as the default for a given type. For more information, see <a href="https://msdn.microsoft.com/78cd05a4-df33-42b5-91b9-826ebce04a1d">Default Programs</a>


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3e9ad8ba-0f0e-46e6-ab0b-61c35bfd2dc6">SetAppAsDefaultAll</a>
</td>
<td align="left" width="63%">
Sets an application as the default for all of the registered associations of any <a href="https://msdn.microsoft.com/library/windows/hardware/hh439450">type</a> for that application.

</td>
</tr>
</table> 


## -remarks



Because <b>IApplicationAssociationRegistration</b> is only supported for Windows Vista and Windows 7, applications that support earlier operating systems must use their preexisting code in relation to defaults when running under those operating systems. Those applications should include a check for the operating system version to account for this.




## -see-also




<a href="https://msdn.microsoft.com/78cd05a4-df33-42b5-91b9-826ebce04a1d">Default Programs</a>
 

 

