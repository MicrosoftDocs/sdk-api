---
UID: NN:oaidl.ICreateTypeLib2
title: ICreateTypeLib2
author: windows-sdk-content
description: Provides the methods for creating and managing the component or file that contains type information.
old-location: automat\icreatetypelib2.htm
tech.root: automat
ms.assetid: 97378353-8c2d-493a-8ee9-42d33ab47d18
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: ICreateTypeLib2, ICreateTypeLib2 interface [Automation], ICreateTypeLib2 interface [Automation],described, _oa96_ICreateTypeLib2_Interface, automat.icreatetypelib2, oaidl/ICreateTypeLib2
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: oaidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OaIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - oaidl.h
api_name:
 - ICreateTypeLib2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICreateTypeLib2 interface


## -description


Provides the methods for creating and managing the component or file that contains type information. Derives from <a href="https://msdn.microsoft.com/d245cd25-ce31-42da-a42d-dc412d5b98e7">ICreateTypeLib</a>. The <a href="https://msdn.microsoft.com/c8bbb677-2666-4900-8fb9-788742eef656">ICreateTypeInfo</a> instance returned from <b>ICreateTypeLib</b> can be accessed through a <b>QueryInterface</b> call to <a href="https://msdn.microsoft.com/34dc6f52-6864-4edb-b22d-80eef05d4c8c">ICreateTypeInfo2</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICreateTypeLib2</b> interface inherits from <b>ICreateTypeLib</b>. <b>ICreateTypeLib2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ICreateTypeLib2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0a233830-631b-4a6d-8fce-eb8f47714e9c">DeleteTypeInfo</a>
</td>
<td align="left" width="63%">
Deletes a specified type information from the type library.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7630a220-c213-4070-90e7-46ce1907127a">SetCustData</a>
</td>
<td align="left" width="63%">
Sets a value to custom data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/35093252-74ff-4161-bf3d-f5e6b69e73c1">SetHelpStringContext</a>
</td>
<td align="left" width="63%">
Sets the Help string context number.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f00a3dbf-7205-48fd-abeb-1d2d80be7743">SetHelpStringDll</a>
</td>
<td align="left" width="63%">
Sets the DLL name to be used for Help string lookup (for localization purposes).

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/aad137b1-b747-4d74-8d6c-5ec9b6e6983d">Type Building Interfaces and Functions </a>
 

 

