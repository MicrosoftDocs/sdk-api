---
UID: NN:wbemcli.IWbemObjectAccess
title: IWbemObjectAccess (wbemcli.h)
description: Provides access to the methods and properties of an object.
old-location: wmi\iwbemobjectaccess.htm
tech.root: WmiSdk
ms.assetid: 1025ae50-870f-4d38-8e83-3c6b628315c6
ms.date: 12/05/2018
ms.keywords: IWbemObjectAccess, IWbemObjectAccess interface [Windows Management Instrumentation], IWbemObjectAccess interface [Windows Management Instrumentation],described, _hmm_iwbemobjectaccess, wbemcli/IWbemObjectAccess, wmi.iwbemobjectaccess
ms.topic: interface
f1_keywords:
- wbemcli/IWbemObjectAccess
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWbemObjectAccess interface


## -description


The 
<b>IWbemObjectAccess</b> interface provides access to the methods and properties of an object.  An 
<b>IWbemObjectAccess</b> object is a container for an instance updated by a <a href="https://docs.microsoft.com/windows/desktop/WmiSdk/gloss-r">refresher</a>. With the 
<b>IWbemObjectAccess</b> interface, you can get and set properties by using property handles instead of object property names.
<div class="alert"><b>Note</b>  This interface is not implemented by client applications or providers under any circumstances. The implementation provided by WMI is the only one that is supported. A pointer to the interface can be retrieved by calling <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q_)">IWbemClassObject::QueryInterface</a>.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWbemObjectAccess</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWbemObjectAccess</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nf-wbemcli-iwbemobjectaccess-getpropertyhandle">GetPropertyHandle</a>
</td>
<td align="left" width="63%">
Returns a unique handle that identifies a property. You can use this handle to identify properties when using 
<b>IWbemObjectAccess</b> methods to read or write property values.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nf-wbemcli-iwbemobjectaccess-getpropertyinfobyhandle">GetPropertyInfoByHandle</a>
</td>
<td align="left" width="63%">
Returns the name and data type of the property that is associated with a property handle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nf-wbemcli-iwbemobjectaccess-lock">Lock</a>
</td>
<td align="left" width="63%">
Prevents other processes from updating an 
<b>IWbemObjectAccess</b> object until it is unlocked.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nf-wbemcli-iwbemobjectaccess-readdword">ReadDWORD</a>
</td>
<td align="left" width="63%">
Reads 32 bits of property data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nf-wbemcli-iwbemobjectaccess-readpropertyvalue">ReadPropertyValue</a>
</td>
<td align="left" width="63%">
Reads a specified number of bytes of property data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nf-wbemcli-iwbemobjectaccess-readqword">ReadQWORD</a>
</td>
<td align="left" width="63%">
Reads 64 bits of property data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nf-wbemcli-iwbemobjectaccess-unlock">Unlock</a>
</td>
<td align="left" width="63%">
Allows other processes to update the property values of an 
<b>IWbemObjectAccess</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nf-wbemcli-iwbemobjectaccess-writedword">WriteDWORD</a>
</td>
<td align="left" width="63%">
Writes 32 bits of property data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nf-wbemcli-iwbemobjectaccess-writepropertyvalue">WritePropertyValue</a>
</td>
<td align="left" width="63%">
Writes a specified number of bytes of property data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nf-wbemcli-iwbemobjectaccess-writeqword">WriteQWORD</a>
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
<a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nf-wbemcli-iwbemclassobject-get">IWbemClassObject::Get</a> and 
<a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nf-wbemcli-iwbemclassobject-put">IWbemClassObject::Put</a>.

<div class="alert"><b>Note</b>  To maximize its speed, 
<b>IWbemObjectAccess</b> is completely unchecked. It is the responsibility of the user to ensure that all handles are proper, and that write buffers are correctly sized. Read and write operations are not intrinsically thread-safe. You should call the 
<a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nf-wbemcli-iwbemobjectaccess-lock">IWbemObjectAccess::Lock</a> and 
<a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nf-wbemcli-iwbemobjectaccess-unlock">IWbemObjectAccess::Unlock</a> methods to prevent 
<b>IWbemObjectAccess</b> objects from concurrent access on multiple threads.</div>
<div> </div>
Property handles are the same for all instances of a class. Therefore, it is only necessary to retrieve a handle one time.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WmiSdk/accessing-performance-data-in-c--">Accessing Performance Data in C++</a>



<a href="https://docs.microsoft.com/windows/desktop/WmiSdk/accessing-wmi-preinstalled-performance-classes">Accessing WMI Preinstalled Performance Classes</a>



<a href="https://docs.microsoft.com/windows/desktop/WmiSdk/com-api-for-wmi">COM API for WMI</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nn-wbemcli-iwbemrefresher">IWbemRefresher</a>
 

 

