---
UID: NN:wcmconfig.ISettingsContext
title: ISettingsContext
author: windows-sdk-content
description: An interface to a backing store that is used to store setting changes made through the other SMI APIs, and provides operations to serialize to and deserialize from a representation.
old-location: smi\isettingscontext.htm
old-project: SMI
ms.assetid: 29f43c3f-57bf-4208-a0bf-9b4414795a59
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: ISettingsContext, ISettingsContext interface [SMI], ISettingsContext interface [SMI],described, smi.isettingscontext, wcmconfig/ISettingsContext
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: wcmconfig.h
req.include-header: 
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
req.typenames: WcmNamespaceAccess
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	SMIEngine.dll
api_name:
-	ISettingsContext
product: Windows
targetos: Windows
req.lib: 
req.dll: SMIEngine.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# ISettingsContext interface


## -description


An interface to a backing store that is used to store setting changes made through the other SMI APIs, and provides operations to serialize to and deserialize from a representation.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISettingsContext</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ISettingsContext</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISettingsContext</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/382f2864-047e-4095-929b-a8b67773eefb">Deserialize</a>
</td>
<td align="left" width="63%">
 Deserializes the data in the provided stream into this context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/844ef731-9ccf-4cf5-9bb9-218312cbb07c">GetNamespaces</a>
</td>
<td align="left" width="63%">
Gets the namespaces that exist in the context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/29ec0b36-31f2-4078-b1a4-872a8ed340e3">GetStoredSettings</a>
</td>
<td align="left" width="63%">
Gets the stored setting changes from the context for the given namespace.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9054edee-9751-4aaa-a9bb-65badfb34fc6">GetUserData</a>
</td>
<td align="left" width="63%">
Gets a user-defined piece of data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/11f541e6-fd97-4756-91c1-44ba2e3d35b1">RevertSetting</a>
</td>
<td align="left" width="63%">
Reverts a setting in the namespace.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/13b29096-8572-4539-abd4-de22a9594f38">Serialize</a>
</td>
<td align="left" width="63%">
Serializes the data in this context into the provided stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4ae754a5-7e03-4747-b4bc-1abf72920d83">SetUserData</a>
</td>
<td align="left" width="63%">
Sets a user-defined piece of data.

</td>
</tr>
</table> 

