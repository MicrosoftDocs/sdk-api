---
UID: NF:objidl.IMoniker.IsSystemMoniker
title: IMoniker::IsSystemMoniker
author: windows-sdk-content
description: Determines whether this moniker is one of the system-provided moniker classes.
old-location: com\imoniker_issystemmoniker.htm
tech.root: com
ms.assetid: a61c0df9-786e-45e7-8b3d-f950decc596d
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: IMoniker interface [COM],IsSystemMoniker method, IMoniker.IsSystemMoniker, IMoniker::IsSystemMoniker, IsSystemMoniker, IsSystemMoniker method [COM], IsSystemMoniker method [COM],IMoniker interface, _com_imoniker_issystemmoniker, com.imoniker_issystemmoniker, objidl/IMoniker::IsSystemMoniker
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ObjIdl.idl
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
 - ObjIdl.h
api_name:
 - IMoniker.IsSystemMoniker
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMoniker::IsSystemMoniker


## -description


Determines whether this moniker is one of the system-provided moniker classes.


## -parameters




### -param pdwMksys [out]

A pointer to a variables that receives one of the values from the <a href="https://msdn.microsoft.com/f0d8ab71-5be9-4a5c-a036-d3a0a90a053f">MKSYS</a> enumeration and refers to one of the COM moniker classes. This parameter cannot be <b>NULL</b>.


## -returns



This method returns S_OK to indicate that the moniker is a system moniker, and S_FALSE otherwise.




## -remarks



<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
New values of the <a href="https://msdn.microsoft.com/f0d8ab71-5be9-4a5c-a036-d3a0a90a053f">MKSYS</a> enumeration may be defined in the future; therefore, you should explicitly test for each value you are interested in.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
Your implementation of this method must return MKSYS_NONE. You cannot use this function to identify your own monikers (for example, in your implementation of <a href="https://msdn.microsoft.com/6e41d79c-1a57-4270-aa84-160e0639852b">IMoniker::ComposeWith</a>). Instead, you should use your moniker's implementation of <a href="https://msdn.microsoft.com/921a3b86-a240-454e-9411-8d653e02b90e">IPersist::GetClassID</a> or use <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> to test for your own private interface.

<h3><a id="Implementation-specific_Notes"></a><a id="implementation-specific_notes"></a><a id="IMPLEMENTATION-SPECIFIC_NOTES"></a>Implementation-specific Notes</h3>
<table>
<tr>
<th>Implementation</th>
<th>Notes</th>
</tr>
<tr>
<td>Anti-moniker</td>
<td>This method returns S_OK and passes back MKSYS_ANTIMONIKER.
</td>
</tr>
<tr>
<td>Class moniker</td>
<td>This method returns S_OK and passes back MKSYS_CLASSMONIKER. 
</td>
</tr>
<tr>
<td>File moniker</td>
<td>This method returns S_OK and passes back MKSYS_CLASSMONIKER. 
</td>
</tr>
<tr>
<td>Generic composite moniker</td>
<td>This method returns S_OK and passes back MKSYS_GENERICCOMPOSITE.
</td>
</tr>
<tr>
<td>Item moniker</td>
<td>This method returns S_OK and passes back MKSYS_ITEMMONIKER.</td>
</tr>
<tr>
<td>OBJREF moniker</td>
<td>This method returns S_OK and passes back MKSYS_OBJREFMONIKER. 
</td>
</tr>
<tr>
<td>Pointer moniker</td>
<td>This method returns S_OK and passes back MKSYS_POINTERMONIKER.
</td>
</tr>
<tr>
<td>URL moniker</td>
<td>This method returns S_OK and passes back MKSYS_URLMONIKER.
</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/17f4c1df-7a9c-42ef-a888-70cd8d85f070">IMoniker</a>
 

 

