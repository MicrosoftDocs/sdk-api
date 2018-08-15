---
UID: NN:wcmconfig.ITargetInfo
title: ITargetInfo
author: windows-sdk-content
description: Defines the offline target information, specifically, file and registry locations as well as wow64 information.
old-location: smi\itargetinfo.htm
old-project: smi
ms.assetid: f1dd3c93-43ca-4804-8330-55acaccf8ea8
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: ITargetInfo, ITargetInfo interface [SMI], ITargetInfo interface [SMI],described, smi.itargetinfo, wcmconfig/ITargetInfo
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: wcmconfig.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WcmConfig.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WcmNamespaceAccess
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - SMIEngine.dll
api_name:
 - ITargetInfo
product: Windows
targetos: Windows
req.lib: 
req.dll: SMIEngine.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ITargetInfo interface


## -description


Defines the offline target information,  specifically, file and registry locations as well as wow64 information.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITargetInfo</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITargetInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITargetInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c9c757f4-ad71-42d7-864a-26f3d1e8000b">ExpandTarget</a>
</td>
<td align="left" width="63%">
Expands a location string to indicate the offline installation location.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7a805c5f-c064-4428-9cfb-1e469450a555">ExpandTargetPath</a>
</td>
<td align="left" width="63%">
Expands a location string to indicate the offline installation location.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2e7854dd-93eb-4626-a67d-4bd3dd79a75b">GetEnumerator</a>
</td>
<td align="left" width="63%">
Gets the enumerator to access the collection of offline properties.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f4366d23-e2dd-4561-af79-870212631ebf">GetProperty</a>
</td>
<td align="left" width="63%">
Gets a property value for the offline installation location.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ad9accbd-0d23-40e6-8132-5a0c63a1b12a">GetSchemaHiveLocation</a>
</td>
<td align="left" width="63%">
Get the location of the schema hive.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d63e3f49-bb7b-4ef6-a573-811b9bbdd9b0">GetSchemaHiveMountName</a>
</td>
<td align="left" width="63%">
Gets the name of the mount location of the schema hive.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b80e3363-8efa-44b7-a61e-66177d1c53ce">GetTargetID</a>
</td>
<td align="left" width="63%">
Gets a unique identifier associated with the current target.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b21137a0-537f-43a4-857b-158a1642ea1c">GetTargetMode</a>
</td>
<td align="left" width="63%">
Gets the current target mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7c66e131-97e6-4a8e-b4b0-927633d6d53a">GetTargetProcessorArchitecture</a>
</td>
<td align="left" width="63%">
Gets processor architecture associated with the current target.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/aebebdee-3a24-4a9b-9ec6-cc411385af41">GetTemporaryStoreLocation</a>
</td>
<td align="left" width="63%">
Gets the current temporary store location.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/863aefc6-d777-4af9-b310-adadef993bcd">LoadModule</a>
</td>
<td align="left" width="63%">
Loads the module from the offline installation location.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4831fdf9-411b-4fdb-bd5c-3a309e6b6918">SetModulePath</a>
</td>
<td align="left" width="63%">
Sets the module path for offline installation location.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ecd93710-a9e8-41cf-b30c-97d1efe0fa6f">SetProperty</a>
</td>
<td align="left" width="63%">
Sets a property value for the offline installation location.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/223ce821-4f31-4673-95e2-ec9cf94d5726">SetSchemaHiveLocation</a>
</td>
<td align="left" width="63%">
Sets the location of the schema hive.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/128cf457-c66e-49b7-88a7-3f5d87800a20">SetSchemaHiveMountName</a>
</td>
<td align="left" width="63%">
Sets the name of the mount location of the schema hive.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/183b1ccd-9244-42d5-a787-617e43a55f64">SetTargetID</a>
</td>
<td align="left" width="63%">
Sets the unique identifier associated with current target.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f8c5e67f-a084-4916-8371-bba4e7fb1da1">SetTargetMode</a>
</td>
<td align="left" width="63%">
Sets the target mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/15056182-4355-48f5-b996-195e3c72235e">SetTargetProcessorArchitecture</a>
</td>
<td align="left" width="63%">
Sets the processor architecture associated with the current target.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ef2b6983-02ff-488a-99ef-9976d76f51b5">SetTemporaryStoreLocation</a>
</td>
<td align="left" width="63%">
Sets the current temporary store location.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8f44485d-0ad3-4c89-a1dc-19610f717972">SetWow64Context</a>
</td>
<td align="left" width="63%">
Sets an opaque context object for wow64 redirection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0325bac8-1843-4e32-97a6-fb6e2bef9e16">TranslateWow64</a>
</td>
<td align="left" width="63%">
Translates paths for wow64 redirection.

</td>
</tr>
</table> 

