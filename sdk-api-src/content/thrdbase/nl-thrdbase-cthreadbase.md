---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# CThreadBase class


## -description


<p class="CCE_Message">[The <b>CThreadBase</b> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

The <b>CThreadBase</b> class is a base class that supplies the internal thread safety mechanisms for the WMI Provider Framework. This class is called internally.

<b xmlns:loc="http://microsoft.com/wdcml/l10n">CThreadBase</b> has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Enumerations</a></li>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul><h3><a id="enums"></a>Enumerations</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">CThreadBase</b> class has these enumerations.
<table>
<tr>
<th align="left" width="37%">Enumeration</th>
<th align="left" width="63%">Description</th>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/B5F1F8DD-9769-40A6-B743-4F4DF4B8C363">FlagDefs</a>
</td>
<td align="left" width="63%">
Specifies which flags are valid for the specified type of operation. This enumeration is used by the <a href="https://msdn.microsoft.com/1d6d1006-99b9-4646-a5c4-835940ce3ac0">Provider::ValidateFlags</a> method.

</td>
</tr>
</table> 
<h3><a id="methods"></a>Methods</h3>The <b>CThreadBase</b> class has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b5c4f714-b411-4a5f-af2b-0bf7ce3c9e70">BeginRead</a>
</td>
<td align="left" width="63%">
Provides thread safety for WMI provider data access when the provider is built on the WMI Provider Framework.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/51ae6b39-b524-4bf9-ac71-45c812ad1680">BeginWrite</a>
</td>
<td align="left" width="63%">
Provides thread safety for WMI provider operations that write data when the provider is built on the WMI Provider Framework.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/43909501-0a65-4728-9a26-30b8391a33c5">CThreadBase</a>
</td>
<td align="left" width="63%">
Initializes a new instance of <b>CThreadBase</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e34fa8bc-f667-4fca-9282-9ca8038f3e75">EndRead</a>
</td>
<td align="left" width="63%">
Provides thread safety by indicating the end of a data read operation when the provider is built on the WMI Provider Framework.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8b57bcc0-f8ca-412a-87d9-9afeb5ac8446">EndWrite</a>
</td>
<td align="left" width="63%">
Provides thread safety by indicating the end of a data write operation when the provider is built on the WMI Provider Framework.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a17a379d-60ba-4a76-8900-58fabadad5ea">OnFinalRelease</a>
</td>
<td align="left" width="63%">
Virtual function called by <a href="_com_iunknown_release">Release</a> when the reference count reaches zero.

</td>
</tr>
</table> 


## -members

The <b>CThreadBase</b> class has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b5c4f714-b411-4a5f-af2b-0bf7ce3c9e70">BeginRead</a>
</td>
<td align="left" width="63%">
Provides thread safety for WMI provider data access when the provider is built on the WMI Provider Framework.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/51ae6b39-b524-4bf9-ac71-45c812ad1680">BeginWrite</a>
</td>
<td align="left" width="63%">
Provides thread safety for WMI provider operations that write data when the provider is built on the WMI Provider Framework.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/43909501-0a65-4728-9a26-30b8391a33c5">CThreadBase</a>
</td>
<td align="left" width="63%">
Initializes a new instance of <b>CThreadBase</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e34fa8bc-f667-4fca-9282-9ca8038f3e75">EndRead</a>
</td>
<td align="left" width="63%">
Provides thread safety by indicating the end of a data read operation when the provider is built on the WMI Provider Framework.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8b57bcc0-f8ca-412a-87d9-9afeb5ac8446">EndWrite</a>
</td>
<td align="left" width="63%">
Provides thread safety by indicating the end of a data write operation when the provider is built on the WMI Provider Framework.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a17a379d-60ba-4a76-8900-58fabadad5ea">OnFinalRelease</a>
</td>
<td align="left" width="63%">
Virtual function called by <a href="_com_iunknown_release">Release</a> when the reference count reaches zero.

</td>
</tr>
</table>Provides thread safety for WMI provider data access when the provider is built on the WMI Provider Framework.

Provides thread safety for WMI provider operations that write data when the provider is built on the WMI Provider Framework.

Initializes a new instance of <b>CThreadBase</b>.

Provides thread safety by indicating the end of a data read operation when the provider is built on the WMI Provider Framework.

Provides thread safety by indicating the end of a data write operation when the provider is built on the WMI Provider Framework.

Virtual function called by <a href="_com_iunknown_release">Release</a> when the reference count reaches zero.

 


## -remarks



The destructor for the class is <b>CWbemGlueFactory::~CWbemGlueFactory</b>.



