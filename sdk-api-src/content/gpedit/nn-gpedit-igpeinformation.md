---
UID: NN:gpedit.IGPEInformation
title: IGPEInformation
author: windows-sdk-content
description: The IGPEInformation interface provides methods for Microsoft Management Console (MMC) extension snap-ins to communicate with the Group Policy Object Editor. For more information about MMC, see the Microsoft Management Console.
old-location: policy\igpeinformation.htm
tech.root: Policy
ms.assetid: 3b3e7793-fc69-43a3-a2b1-0aa36748a19b
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IGPEInformation, IGPEInformation interface [Group Policy], IGPEInformation interface [Group Policy],described, _win32_igpeinformation, gpedit/IGPEInformation, policy.igpeinformation
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: gpedit.h
req.include-header: 
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
req.lib: 
req.dll: Gpedit.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gpedit.dll
api_name:
 - IGPEInformation
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IGPEInformation interface


## -description


The
    <b>IGPEInformation</b> interface provides methods for Microsoft Management Console (MMC) extension snap-ins to communicate with the Group Policy Object Editor. For more information about MMC, see the 
<a href="https://msdn.microsoft.com/afa61d59-a568-469d-832a-b69e766a0207">Microsoft Management Console</a>.

Note that this interface does not support multithreaded object concurrency.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IGPEInformation</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IGPEInformation</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IGPEInformation</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3c1a43a5-5d16-4abc-85e0-1eeace2ee086">GetDisplayName</a>
</td>
<td align="left" width="63%">
Retrieves the display name for a GPO.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0cf969b2-40a9-4fbd-ba2b-38979fb5796a">GetDSPath</a>
</td>
<td align="left" width="63%">
Retrieves the Active Directory path for a section of the GPO.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6fcdc7f8-61bf-4d3e-b0aa-ff730d6730cb">GetFileSysPath</a>
</td>
<td align="left" width="63%">
Returns the file system path for a section of the GPO.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4e63c6b7-ae4f-4789-bfcc-8a066fb6ad02">GetHint</a>
</td>
<td align="left" width="63%">
Retrieves the type of Active Directory object to which a GPO can be linked.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/94112a6e-cd8a-4fb7-9c37-86a1b7713ddb">GetName</a>
</td>
<td align="left" width="63%">
Retrieves the unique name for a GPO, usually a GUID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/22c90ec4-b4cc-4a95-becd-29c2ce6e3c29">GetOptions</a>
</td>
<td align="left" width="63%">
Retrieves the options the user has selected for the Group Policy Object Editor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/23ccca67-6e49-44d1-b69e-e72b9095bed8">GetRegistryKey</a>
</td>
<td align="left" width="63%">
Retrieves a handle to the root of the registry key for a section of the GPO.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/47769405-d32c-4f4f-86fc-970d89bba848">GetType</a>
</td>
<td align="left" width="63%">
Retrieves type information for the GPO being edited.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4c36fbcb-2adb-4c32-87d3-efcd55dbaf3e">PolicyChanged</a>
</td>
<td align="left" width="63%">
Informs the Group Policy Object Editor that policy settings have changed.

</td>
</tr>
</table> 


## -remarks



To create and modify a GPO directly, without using the Group Policy Object Editor, see the methods of the 
<a href="https://msdn.microsoft.com/b3cd31a1-c238-4eb2-8164-9c4891e6227b">IGroupPolicyObject</a> interface.




## -see-also




<a href="https://msdn.microsoft.com/dc15a69d-a44d-4731-a9e5-6165abd581c4">Group Policy Interfaces</a>



<a href="https://msdn.microsoft.com/1285ab5a-ea68-4c16-bc34-8ab2f3cfad35">Group Policy Overview</a>
 

 

