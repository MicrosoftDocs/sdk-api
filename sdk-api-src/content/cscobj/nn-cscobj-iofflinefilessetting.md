---
UID: NN:cscobj.IOfflineFilesSetting
title: IOfflineFilesSetting (cscobj.h)
author: windows-sdk-content
description: Represents a setting that controls the behavior the Offline Files service.
old-location: of\iofflinefilessetting.htm
tech.root: offlinefiles
ms.assetid: 6f47c67b-9438-4229-89b2-6b3f9da8fb68
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IOfflineFilesSetting, IOfflineFilesSetting interface [Offline Files], IOfflineFilesSetting interface [Offline Files],described, cscobj/IOfflineFilesSetting, of.iofflinefilessetting
ms.topic: interface
req.header: cscobj.h
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
req.dll: CscSvc.dll; CscObj.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CscSvc.dll
 - CscObj.dll
api_name:
 - IOfflineFilesSetting
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOfflineFilesSetting interface


## -description


Represents a setting that controls the behavior the Offline Files service.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOfflineFilesSetting</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IOfflineFilesSetting</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IOfflineFilesSetting</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/815791e8-3e41-4511-9789-9b9258e5fcf4">DeletePreference</a>
</td>
<td align="left" width="63%">
Removes a preference setting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2e4591b5-c8a9-4645-8001-8ac09c706ee2">GetName</a>
</td>
<td align="left" width="63%">
Retrieves a name associated with a particular Offline Files setting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b7f7f8f5-2640-4770-a7ba-230cca8a9575">GetPolicy</a>
</td>
<td align="left" width="63%">
Retrieves a policy associated with a particular Offline Files setting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/29f6d96f-c873-4cc3-88f2-cd075b3ec004">GetPolicyScope</a>
</td>
<td align="left" width="63%">
Indicates the scope of the policy associated with this setting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/80bc64f2-2787-42ba-9c36-742964440f74">GetPreference</a>
</td>
<td align="left" width="63%">
Retrieves a per-machine or per-user preference associated with a particular Offline Files setting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/618a83b7-a86d-4356-8312-7aba8923e8a4">GetPreferenceScope</a>
</td>
<td align="left" width="63%">
Retrieves the scope of the preference associated with this setting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/39560ca6-62d7-467b-bc52-1dd769e7e860">GetValue</a>
</td>
<td align="left" width="63%">
Retrieves the value of a particular Offline Files setting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2b5567bf-a7c6-40b3-ac16-9da805ddb3b3">GetValueType</a>
</td>
<td align="left" width="63%">
Retrieves the data type of a particular Offline Files setting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a5dc0522-4a1b-450f-bddb-17e67007f809">SetPreference</a>
</td>
<td align="left" width="63%">
Sets a per-computer or per-user preference associated with an Offline Files setting.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/9dea396f-ab71-4b2e-b5d3-776c16614f26">Offline Files API Interfaces</a>
 

 

