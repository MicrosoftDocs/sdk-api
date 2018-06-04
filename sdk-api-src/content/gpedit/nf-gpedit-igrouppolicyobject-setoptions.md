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

# IGroupPolicyObject::SetOptions


## -description


The
    <b>SetOptions</b> method sets the options for the GPO.


## -parameters




### -param dwOptions [in]

Specifies the new option values. This parameter can be one or more of the following options. For more information, see the following Remarks section.



#### GPO_OPTION_DISABLE_USER

Disable the user portion of the GPO.



#### GPO_OPTION_DISABLE_MACHINE

Disable the computer portion of the GPO.


### -param dwMask [in]

Specifies the options to change. This parameter can be one or more of the following options. For more information, see the following Remarks section.



#### GPO_OPTION_DISABLE_USER

Disable the user portion of the GPO.



#### GPO_OPTION_DISABLE_MACHINE

Disable the computer portion of the GPO.


## -returns



If the method succeeds, the return value is <b>S_OK</b>. Otherwise, the method returns one of the COM error codes defined in the Platform SDK header file WinError.h.




## -remarks



<div class="alert"><b>Note</b>  A policy refresh will be automatically triggered when the user or computer portion of the local Group Policy object is enabled or disabled using the  <b>SetOptions</b> method.</div>
<div> </div>
To change an option, you must set the appropriate flag in the <i>dwMask</i> parameter. If the flag is set, then the system reads the <i>dwOptions</i> parameter to set the new state. For example, to disable the user portion of a GPO, and leave the computer portion unchanged, call the 
<b>SetOptions</b> method as follows:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>SetOptions(GPO_OPTION_DISABLE_USER, GPO_OPTION_DISABLE_USER)</pre>
</td>
</tr>
</table></span></div>
To enable the user portion and disable the computer portion, call the 
<b>SetOptions</b> method as follows:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>SetOptions(GPO_OPTION_DISABLE_MACHINE, GPO_OPTION_DISABLE_USER | GPO_OPTION_DISABLE_MACHINE)</pre>
</td>
</tr>
</table></span></div>
To retrieve the options for a GPO, you can call the 
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451244">GetOptions</a> method.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/hh451244">GetOptions</a>



<a href="https://msdn.microsoft.com/dc15a69d-a44d-4731-a9e5-6165abd581c4">Group Policy
    Interfaces</a>



<a href="https://msdn.microsoft.com/1285ab5a-ea68-4c16-bc34-8ab2f3cfad35">Group Policy
    Overview</a>



<a href="https://msdn.microsoft.com/b3cd31a1-c238-4eb2-8164-9c4891e6227b">IGroupPolicyObject</a>
 

 

