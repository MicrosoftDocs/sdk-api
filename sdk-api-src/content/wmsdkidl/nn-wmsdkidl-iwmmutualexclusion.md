---
UID: NN:wmsdkidl.IWMMutualExclusion
title: IWMMutualExclusion
author: windows-sdk-content
description: The IWMMutualExclusion interface represents a group of streams, of which only one at a time can be played.IWMMutualExclusion is the base interface for mutual exclusion objects.
old-location: wmformat\iwmmutualexclusion.htm
old-project: wmformat
ms.assetid: 040635fb-de00-4c8c-9c39-c28c409311c3
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: IWMMutualExclusion, IWMMutualExclusion interface [windows Media Format], IWMMutualExclusion interface [windows Media Format],described, IWMMutualExclusionInterface, wmformat.iwmmutualexclusion, wmsdkidl/IWMMutualExclusion
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: wmsdkidl.h
req.include-header: 
req.target-type: Windows
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
tech.root: 
req.typenames: WM_AETYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmsdkidl.h
api_name:
 - IWMMutualExclusion
product: Windows
targetos: Windows
req.lib: Wmvcore.lib
req.dll: Wmvcore.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMMutualExclusion interface


## -description



The <b>IWMMutualExclusion</b> interface represents a group of streams, of which only one at a time can be played.

<b>IWMMutualExclusion</b> is the base interface for mutual exclusion objects. You can create a mutual exclusion object only as part of a profile. Never use COM functions, such as <b>CoCreateInstance</b>, to create a mutual exclusion object. Instead, you must already have a profile opened and make a call to its <a href="https://msdn.microsoft.com/fcf3a549-5ae1-459a-95b9-923570f59a4a">IWMProfile::CreateNewMutualExclusion</a> method. After a mutual exclusion object has been created, you can change the type of mutual exclusion by using the methods in this interface.

You can manage the streams in a mutual exclusion object using the methods of the <a href="https://msdn.microsoft.com/076bb0bf-3cf8-48b4-bfca-abbd9c1bf211">IWMStreamList</a> interface. <b>IWMMutualExclusion</b> inherits from <b>IWMStreamList</b>, so those methods are directly available in this interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMMutualExclusion</b> interface inherits from <a href="https://msdn.microsoft.com/076bb0bf-3cf8-48b4-bfca-abbd9c1bf211">IWMStreamList</a>. <b>IWMMutualExclusion</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMMutualExclusion</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/jj991813">GetType</a>
</td>
<td align="left" width="63%">
Retrieves the GUID of the type of mutual exclusion required.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/jj991816">SetType</a>
</td>
<td align="left" width="63%">
Specifies the GUID of the type of mutual exclusion required.

</td>
</tr>
</table> 

The following interface can be obtained by using the QueryInterface method of this interface.

<table>
<tr>
<th>Interface</th>
<th>IID</th>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/076bb0bf-3cf8-48b4-bfca-abbd9c1bf211">IWMStreamList</a>
</td>
<td>IID_IWMStreamList</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/4a1f468c-2ba5-48a1-b56f-8b62aacf1ccf">IWMMutualExclusion2</a>
</td>
<td>IID_IWMMutualExclusion2</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/e5ec945c-4513-48ad-8bef-e0fb54826991">IWMProfileManager Interface</a>



<a href="https://msdn.microsoft.com/076bb0bf-3cf8-48b4-bfca-abbd9c1bf211">IWMStreamList</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn965732">Interfaces</a>



<a href="https://msdn.microsoft.com/8d174243-334e-418e-a1c8-77486b940de7">Profile Manager Object</a>
 

 

