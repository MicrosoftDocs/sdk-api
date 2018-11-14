---
UID: NN:wmsdkidl.IWMProfile2
title: IWMProfile2
author: windows-sdk-content
description: The IWMProfile2 interface exposes the globally unique identifier for a system profile.
old-location: wmformat\iwmprofile2.htm
tech.root: wmformat
ms.assetid: 34e30edb-3247-4eaa-9a63-6d94c9e37c0b
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: IWMProfile2, IWMProfile2 interface [windows Media Format], IWMProfile2 interface [windows Media Format],described, IWMProfile2Interface, wmformat.iwmprofile2, wmsdkidl/IWMProfile2
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmsdkidl.h
api_name:
 - IWMProfile2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMProfile2 interface


## -description



The <b>IWMProfile2</b> interface exposes the globally unique identifier for a system profile. System profiles have associated identifiers, but custom profiles do not.

As with <a href="https://msdn.microsoft.com/00f28d6b-d27d-4268-960e-c8ea25e5359e">IWMProfile</a>, <b>IWMProfile2</b> is included in profile objects as well as in reader and synchronous reader objects. To obtain a pointer to an <b>IWMProfile2</b> interface, call the <b>QueryInterface</b> method of any interface in one of these objects. For more information, see <b>IWMProfile Interface</b>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMProfile2</b> interface inherits from <a href="https://msdn.microsoft.com/00f28d6b-d27d-4268-960e-c8ea25e5359e">IWMProfile</a>. <b>IWMProfile2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMProfile2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/82e3e086-4b19-4eb9-91ad-d30392f97a28">GetProfileID</a>
</td>
<td align="left" width="63%">
Retrieves the globally unique identifier of the profile.

</td>
</tr>
</table> 

For information about which interfaces can be obtained by using the QueryInterface method of this interface, see the topic for the object on which this interface is implemented.



## -see-also




<a href="https://msdn.microsoft.com/00f28d6b-d27d-4268-960e-c8ea25e5359e">IWMProfile Interface</a>



<a href="https://msdn.microsoft.com/e5ec945c-4513-48ad-8bef-e0fb54826991">IWMProfileManager Interface</a>



<a href="https://msdn.microsoft.com/c61a0739-09f2-497f-a2cd-d3f2472738e3">Interfaces</a>



<a href="https://msdn.microsoft.com/8d174243-334e-418e-a1c8-77486b940de7">Profile Manager Object</a>



<a href="https://msdn.microsoft.com/e1e31632-0db7-47db-a992-f5db9d8824c1">Working with Profiles</a>
 

 

