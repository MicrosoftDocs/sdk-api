---
UID: NN:wbemcli.IEnumWbemClassObject
title: IEnumWbemClassObject
author: windows-sdk-content
description: The IEnumWbemClassObject interface is used to enumerate Common Information Model (CIM) objects and is similar to a standard COM enumerator.
old-location: wmi\ienumwbemclassobject.htm
old-project: WmiSdk
ms.assetid: 142ea48d-d47b-4b7b-ab84-049a54955488
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: IEnumWbemClassObject, IEnumWbemClassObject interface [Windows Management Instrumentation], IEnumWbemClassObject interface [Windows Management Instrumentation],described, _hmm_ienumwbemclassobject, wbemcli/IEnumWbemClassObject, wmi.ienumwbemclassobject
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: WMI_OBJ_TEXT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Fastprox.dll
api_name:
 - IEnumWbemClassObject
product: Windows
targetos: Windows
req.lib: Wbemuuid.lib
req.dll: Fastprox.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IEnumWbemClassObject interface


## -description


The 
<b>IEnumWbemClassObject</b> interface is used to enumerate <a href="gloss_c.htm">Common Information Model</a> (CIM) objects and is similar to a standard COM enumerator.

An object of type 
<b>IEnumWbemClassObject</b> is received from calls to the following methods:
<ul>
<li>
<a href="https://msdn.microsoft.com/8cb4a42b-f8ae-4a6f-884c-fa808b11dc8a">IWbemServices::ExecQuery</a>
</li>
<li>
<a href="https://msdn.microsoft.com/47671b9b-a2ff-4375-b2a4-7e8599f1fb69">IWbemServices::CreateInstanceEnum</a>
</li>
<li>
<a href="https://msdn.microsoft.com/23122b38-5671-4454-be79-85c6bc34daa0">IWbemServices::CreateClassEnum</a>
</li>
<li>
<a href="https://msdn.microsoft.com/fe547660-4095-4a75-829d-f06599c0d9d7">IWbemServices::ExecNotificationQuery</a>
</li>
</ul>CIM objects are retrieved from an enumeration as objects of type 
<a href="https://msdn.microsoft.com/a3ce37d7-5580-4b84-9119-78412c8e0d27">IWbemClassObject</a> by calling the 
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926903">Next</a> method. You can reset an enumeration back to the beginning by calling the 
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926942">Reset</a> method.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumWbemClassObject</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IEnumWbemClassObject</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumWbemClassObject</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn938510">Clone</a>
</td>
<td align="left" width="63%">
Makes a copy of the enumerator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926903">Next</a>
</td>
<td align="left" width="63%">
Retrieves the next object or objects in the enumeration starting from the current position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1ff82982-a2d7-4618-8488-9e4b7628012d">NextAsync</a>
</td>
<td align="left" width="63%">
Retrieves the next object or objects using asynchronous integration with 
<a href="https://msdn.microsoft.com/987aea1d-912a-4691-987f-181c1ef1a8a9">IWbemObjectSink</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926942">Reset</a>
</td>
<td align="left" width="63%">
Resets an enumeration sequence back to the beginning.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926952">Skip</a>
</td>
<td align="left" width="63%">
Causes the enumeration to skip ahead so that future calls to the 
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926903">Next</a> method retrieve objects one, or more, ahead of the current location in the enumeration.

</td>
</tr>
</table> 


## -remarks



<b>IEnumWbemClassObject</b> is the object returned from a WMI query, and is used to enumerate through the returned values. For more information on how to use this class, see <a href="https://msdn.microsoft.com/0cceda42-fba0-4a08-90dd-43f022d0be41">Querying WMI</a> and <a href="https://msdn.microsoft.com/fe7e3259-9a7c-4f73-af30-192bbbace1b3">Enumerating WMI</a>.


#### Examples

The following C++ code sample describes how to retrieve an <b>IEnumWbemClassObject</b>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>void ExecQuerySync(IWbemServices *pSvc)
{
    // Query for all users and groups.

    BSTR Language = SysAllocString(L"WQL");
    BSTR Query = SysAllocString(L"SELECT * FROM __Namespace");

    // Initialize the IEnumWbemClassObject pointer.
    IEnumWbemClassObject *pEnum = 0;

    // Issue the query.
    HRESULT hRes = pSvc-&gt;ExecQuery(
        Language,
        Query,
        WBEM_FLAG_FORWARD_ONLY,         // Flags
        0,                              // Context
        &amp;pEnum
        );

    SysFreeString(Query);
    SysFreeString(Language);

    if (hRes != 0)
    {
        printf("Error\n");
        return;
    }
    
    ULONG uTotal = 0;

    // Retrieve the objects in the result set.
    for (;;)
    {
        IWbemClassObject *pObj = 0;
        ULONG uReturned = 0;

        hRes = pEnum-&gt;Next(
            0,                  // Time out
            1,                  // One object
            &amp;pObj,
            &amp;uReturned
            );

        uTotal += uReturned;

        if (uReturned == 0)
            break;

        // Use the object.
        
        // ...
        
        // Release it.
        // ===========
        
        pObj-&gt;Release();    // Release objects not owned.            
    }

    // All done.
    pEnum-&gt;Release();
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/5fa8f1b5-fd19-4d45-9b53-bc7089eecdb1">COM API for
    WMI</a>



<a href="https://msdn.microsoft.com/fe7e3259-9a7c-4f73-af30-192bbbace1b3">Enumerating WMI</a>
 

 

