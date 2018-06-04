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

# CryptCATEnumerateMember function


## -description


<p class="CCE_Message">[The <b>CryptCATEnumerateMember</b> function is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

The <b>CryptCATEnumerateMember</b> function enumerates the members of a catalog.


## -parameters




### -param hCatalog [in]

The handle of the catalog that contains the members to enumerate. This value cannot be <b>NULL</b>.


### -param pPrevMember [in]

A pointer to a <a href="https://msdn.microsoft.com/08f663d9-9dc2-4ac9-95c5-7f2ed972eb9b">CRYPTCATMEMBER</a> structure that identifies which member of the catalog was last retrieved. If this parameter is <b>NULL</b>, this function will retrieve the first member of the catalog.


## -returns



This function returns a pointer to a <a href="https://msdn.microsoft.com/08f663d9-9dc2-4ac9-95c5-7f2ed972eb9b">CRYPTCATMEMBER</a> structure that represents the next member of the catalog. If there are no more members in the catalog to enumerate, this function returns <b>NULL</b>.




## -remarks



Do not free the returned pointer nor any of the members pointed to by the returned pointer.


#### Examples

The following pseudocode example shows how to use this function to enumerate all of the members of a catalog.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>CRYPTCATMEMBER *pMember = NULL;

for(pMember = CryptCATEnumerateMember(hCatalog, pMember); 
    NULL != pMember; 
    pMember = CryptCATEnumerateMember(hCatalog, pMember))
{
   // Use the catalog member.
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/08f663d9-9dc2-4ac9-95c5-7f2ed972eb9b">CRYPTCATMEMBER</a>
 

 

