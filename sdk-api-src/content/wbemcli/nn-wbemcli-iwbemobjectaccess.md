---
UID: NN:wbemcli.IWbemObjectAccess
title: IWbemObjectAccess
author: windows-sdk-content
description: Provides access to the methods and properties of an object.
old-location: wmi\iwbemobjectaccess.htm
tech.root: WmiSdk
ms.assetid: 1025ae50-870f-4d38-8e83-3c6b628315c6
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWbemObjectAccess, IWbemObjectAccess interface [Windows Management Instrumentation], IWbemObjectAccess interface [Windows Management Instrumentation],described, _hmm_iwbemobjectaccess, wbemcli/IWbemObjectAccess, wmi.iwbemobjectaccess
ms.topic: interface
req.header: wbemcli.h
req.include-header: Wbemidl.h
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
req.lib: Wbemuuid.lib
req.dll: Esscli.dll; Fastprox.dll; Wbemess.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Esscli.dll
 - Fastprox.dll
 - Wbemess.dll
api_name:
 - IWbemObjectAccess
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWbemObjectAccess interface


## -description


The 
<b>IWbemObjectAccess</b> interface provides access to the methods and properties of an object.  An 
<b>IWbemObjectAccess</b> object is a container for an instance updated by a <a href="https://msdn.microsoft.com/en-us/library/Aa390834(v=VS.85).aspx">refresher</a>. With the 
<b>IWbemObjectAccess</b> interface, you can get and set properties by using property handles instead of object property names.
<div class="alert"><b>Note</b>  This interface is not implemented by client applications or providers under any circumstances. The implementation provided by WMI is the only one that is supported. A pointer to the interface can be retrieved by calling <a href="https://msdn.microsoft.com/en-us/library/ms682521(v=VS.85).aspx">IWbemClassObject::QueryInterface</a>.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWbemObjectAccess</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWbemObjectAccess</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWbemObjectAccess</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/889d90cd-f53f-460e-b1c2-ed2b87863d58">GetPropertyHandle</a>
</td>
<td align="left" width="63%">
Returns a unique handle that identifies a property. You can use this handle to identify properties when using 
<b>IWbemObjectAccess</b> methods to read or write property values.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a29157a8-50da-485d-a2b1-bf9645ba9963">GetPropertyInfoByHandle</a>
</td>
<td align="left" width="63%">
Returns the name and data type of the property that is associated with a property handle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c2d4f821-aa6f-48d7-8645-192afe48c30c">Lock</a>
</td>
<td align="left" width="63%">
Prevents other processes from updating an 
<b>IWbemObjectAccess</b> object until it is unlocked.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5352dea3-6d10-42be-aa1e-786ace193827">ReadDWORD</a>
</td>
<td align="left" width="63%">
Reads 32 bits of property data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/878fa803-73dc-45ad-8d58-2decb7e316b2">ReadPropertyValue</a>
</td>
<td align="left" width="63%">
Reads a specified number of bytes of property data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cb76eb26-e407-411a-9ccb-a03eaa8bf22e">ReadQWORD</a>
</td>
<td align="left" width="63%">
Reads 64 bits of property data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a1b841b2-684e-4697-b802-b0534f752a13">Unlock</a>
</td>
<td align="left" width="63%">
Allows other processes to update the property values of an 
<b>IWbemObjectAccess</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a1716599-69ba-44fb-be68-b22578f6c6b2">WriteDWORD</a>
</td>
<td align="left" width="63%">
Writes 32 bits of property data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2ac2b8b0-8b69-4f01-8017-ace82a382f40">WritePropertyValue</a>
</td>
<td align="left" width="63%">
Writes a specified number of bytes of property data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f0d098b7-06f4-4a0a-8db9-fa1ef9be4468">WriteQWORD</a>
</td>
<td align="left" width="63%">
Writes 64 bits of property data.

</td>
</tr>
</table> 


## -remarks



The 
<b>IWbemObjectAccess</b> methods that read and write data perform very little data validation. Because 
<b>IWbemObjectAccess</b> methods directly access properties, you can get and set properties much more rapidly than you can using standard object access techniques such as 
<a href="https://msdn.microsoft.com/e4f6c28b-42d7-4109-803e-d3aac4d8509e">IWbemClassObject::Get</a> and 
<a href="https://msdn.microsoft.com/7b67739f-5c67-447a-a1a5-fad9ce3e857a">IWbemClassObject::Put</a>.

<div class="alert"><b>Note</b>  To maximize its speed, 
<b>IWbemObjectAccess</b> is completely unchecked. It is the responsibility of the user to ensure that all handles are proper, and that write buffers are correctly sized. Read and write operations are not intrinsically thread-safe. You should call the 
<a href="https://msdn.microsoft.com/c2d4f821-aa6f-48d7-8645-192afe48c30c">IWbemObjectAccess::Lock</a> and 
<a href="https://msdn.microsoft.com/a1b841b2-684e-4697-b802-b0534f752a13">IWbemObjectAccess::Unlock</a> methods to prevent 
<b>IWbemObjectAccess</b> objects from concurrent access on multiple threads.</div>
<div> </div>
Property handles are the same for all instances of a class. Therefore, it is only necessary to retrieve a handle one time.




## -see-also




<a href="https://msdn.microsoft.com/ee0a2ead-f53a-4651-a287-04a62eba3f84">Accessing Performance Data in C++</a>



<a href="https://msdn.microsoft.com/2158385f-d0dc-4102-84db-ce02d2b0ee53">Accessing WMI Preinstalled Performance Classes</a>



<a href="https://msdn.microsoft.com/5fa8f1b5-fd19-4d45-9b53-bc7089eecdb1">COM API for WMI</a>



<a href="https://msdn.microsoft.com/cd1d652a-f0ce-401c-9a5e-074e6bb4d9ed">IWbemRefresher</a>
 

 

