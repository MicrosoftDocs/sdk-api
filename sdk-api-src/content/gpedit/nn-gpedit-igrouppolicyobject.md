---
UID: NN:gpedit.IGroupPolicyObject
title: IGroupPolicyObject
author: windows-sdk-content
description: The IGroupPolicyObject interface provides methods to create and modify a GPO directly, without using the Group Policy Object Editor.
old-location: policy\igrouppolicyobject.htm
old-project: Policy
ms.assetid: b3cd31a1-c238-4eb2-8164-9c4891e6227b
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IGroupPolicyObject, IGroupPolicyObject interface [Group Policy], IGroupPolicyObject interface [Group Policy],described, _win32_igrouppolicyobject, gpedit/IGroupPolicyObject, policy.igrouppolicyobject
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: gpedit.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gpedit.dll
api_name:
 - IGroupPolicyObject
product: Windows
targetos: Windows
req.lib: 
req.dll: Gpedit.dll
req.irql: 
req.product: GDI+ 1.1
---

# IGroupPolicyObject interface


## -description


The
    <b>IGroupPolicyObject</b> interface provides methods to create and modify a GPO directly, without using the Group Policy Object Editor.

Note that this interface does not support multithreaded object concurrency.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IGroupPolicyObject</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IGroupPolicyObject</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IGroupPolicyObject</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/34afb04e-47f9-4d7c-9fa6-9d76188d7e05">Delete</a>
</td>
<td align="left" width="63%">
Deletes the GPO.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a16592c3-8fa1-4859-b379-ef31999a3fdd">GetDisplayName</a>
</td>
<td align="left" width="63%">
Retrieves the display name for the GPO.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0d6d0b3d-5ad4-4363-a123-f074193b75e2">GetDSPath</a>
</td>
<td align="left" width="63%">
Retrieves the Active Directory path to the root of the specified GPO section.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9f0837ff-31bb-4eaa-82e4-ef127f8e605a">GetFileSysPath</a>
</td>
<td align="left" width="63%">
Retrieves the file system path (UNC format) to the root of the specified GPO section.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6ac20718-45d4-4a45-a95e-d159e4d6dacc">GetMachineName</a>
</td>
<td align="left" width="63%">
Retrieves the computer name of the remote GPO.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1374c01c-aba3-48f5-8a42-7139873d8f7c">GetName</a>
</td>
<td align="left" width="63%">
Retrieves the unique name for the GPO.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a4b86196-04c8-4ec1-bf26-2a33e44020d2">GetOptions</a>
</td>
<td align="left" width="63%">
Retrieves the options for the GPO.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ecfecaa4-eb6e-4de6-a5fe-ecd0e9df886c">GetPath</a>
</td>
<td align="left" width="63%">
Retrieves the path to the GPO.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d464d5fc-64f0-4f34-bcc0-35d92e65f79b">GetPropertySheetPages</a>
</td>
<td align="left" width="63%">
Retrieves the property sheet pages associated with the GPO.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6d46aeb4-8675-4746-9b80-46a0def184b8">GetRegistryKey</a>
</td>
<td align="left" width="63%">
Retrieves a handle to the root of the registry key for the specified GPO section.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e64314aa-340f-496c-aa6b-4744573565f6">GetType</a>
</td>
<td align="left" width="63%">
Retrieves type information for the GPO being edited.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e251cac2-8fc8-4ed0-b940-4a9f47eca26b">New</a>
</td>
<td align="left" width="63%">
Creates a new GPO in the Active Directory with the specified display name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/362b6229-d73f-424f-b906-05ed43e5e034">OpenDSGPO</a>
</td>
<td align="left" width="63%">
Opens the specified GPO and optionally loads the registry information.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c986152b-59cd-4733-bcdd-ee7f0b6907ad">OpenLocalMachineGPO</a>
</td>
<td align="left" width="63%">
Opens the default GPO for the computer and optionally loads the registry information.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ac124b48-7eb6-473b-a96b-de9b1a903f28">OpenRemoteMachineGPO</a>
</td>
<td align="left" width="63%">
Opens the default GPO for the specified remote computer and optionally loads the registry information.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e3713e5f-c710-48f7-8081-f2669c77449d">Save</a>
</td>
<td align="left" width="63%">
Saves the specified registry policy settings to disk and updates the revision number of the GPO.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/979e8399-83e1-421e-8f32-813464ac97aa">SetDisplayName</a>
</td>
<td align="left" width="63%">
Sets the display name for the GPO.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4caed430-2861-49cb-9418-b12bf1c46707">SetOptions</a>
</td>
<td align="left" width="63%">
Sets the options for the GPO.

</td>
</tr>
</table> 


## -remarks



For methods that Microsoft Management Console (MMC) extension snap-ins can use to communicate with the Group Policy Object Editor, see the 
<a href="https://msdn.microsoft.com/3b3e7793-fc69-43a3-a2b1-0aa36748a19b">IGPEInformation</a> interface.




## -see-also




<a href="https://msdn.microsoft.com/dc15a69d-a44d-4731-a9e5-6165abd581c4">Group Policy Interfaces</a>



<a href="https://msdn.microsoft.com/1285ab5a-ea68-4c16-bc34-8ab2f3cfad35">Group Policy Overview</a>
 

 

