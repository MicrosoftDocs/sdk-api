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

# tagRootCauseInfo structure


## -description


Contains detailed information about the root cause of an incident.


## -struct-fields




### -field pwszDescription

Type: <b>LPWSTR</b>

A string that describes the problem that caused the incident.


### -field rootCauseID

Type: <b>GUID</b>

The GUID that corresponds to the problem identified.


### -field rootCauseFlags

Type: <b>DWORD</b>

A numeric value that provides more information about the problem.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="RCF_ISLEAF"></a><a id="rcf_isleaf"></a><dl>
<dt><b>RCF_ISLEAF</b></dt>
<dt>0x1</dt>
</dl>
</td>
<td width="60%">
The root cause corresponds to a leaf in the diagnostics tree. Root causes that are leafs are more likely to be closer to the problem that the user is trying to diagnose. 

</td>
</tr>
<tr>
<td width="40%"><a id="RCF_ISCONFIRMED"></a><a id="rcf_isconfirmed"></a><dl>
<dt><b>RCF_ISCONFIRMED</b></dt>
<dt>0x2</dt>
</dl>
</td>
<td width="60%">
The root cause corresponds to a node with a <a href="https://msdn.microsoft.com/2ad72ac5-3f33-4206-be39-1cfe11ee840d">DIAGNOSIS_STATUS</a> value of <b>DS_CONFIRMED</b>. Problems with confirmed low health are more likely to correspond to the problem the user is trying to diagnose. 

</td>
</tr>
<tr>
<td width="40%"><a id="RCF_ISTHIRDPARTY"></a><a id="rcf_isthirdparty"></a><dl>
<dt><b>RCF_ISTHIRDPARTY</b></dt>
<dt>0x4</dt>
</dl>
</td>
<td width="60%">
The root cause comes from a third-party helper class extension rather than a native Windows helper class.

</td>
</tr>
</table>
 


### -field networkInterfaceID

Type: <b>GUID</b>

GUID of the network interface on which the problem occurred. If the problem is not interface-specific, this value is zero (0).  


### -field pRepairs

Type: <b><a href="https://msdn.microsoft.com/9357f463-946c-47ad-bb8d-ff9de210e7e1">RepairInfoEx</a>*</b>

The repairs that are available to try and fix the problem.


### -field repairCount

Type: <b>USHORT</b>

The number of repairs available. 


## -see-also




<a href="https://msdn.microsoft.com/6bcd1341-657a-40c1-bebd-1c0f780ae337">CopyRootCauseInfo</a>



<a href="https://msdn.microsoft.com/2ad72ac5-3f33-4206-be39-1cfe11ee840d">DIAGNOSIS_STATUS</a>



<a href="https://msdn.microsoft.com/b45fa432-0db4-470b-80ce-ae25c33f88d6">FreeRootCauseInfos</a>



<a href="https://msdn.microsoft.com/9357f463-946c-47ad-bb8d-ff9de210e7e1">RepairInfoEx</a>
 

 

