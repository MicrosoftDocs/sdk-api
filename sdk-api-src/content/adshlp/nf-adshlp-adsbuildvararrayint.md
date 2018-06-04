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

# ADsBuildVarArrayInt function


## -description


The <b>ADsBuildVarArrayInt</b> function builds a variant array of integers from an array of <b>DWORD</b> values.


## -parameters




### -param lpdwObjectTypes [in]

Type: <b>LPDWORD</b>

Array of <b>DWORD</b> values.


### -param dwObjectTypes [in]

Type: <b>DWORD</b>

Number of <b>DWORD</b> entries in the given array.


### -param pVar [out]

Type: <b>VARIANT*</b>

Pointer to the resulting variant array of integers.


## -returns



Type: <b>HRESULT</b>

This method supports standard return values.

For more information about other return values, see  <a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>.




## -remarks



Use the <b>ADsBuildVarArrayInt</b> function to convert the integer array into a variant array of the integers. The following code example shows how to do this.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>DWORD dwArray[]={0,1,2,3,4};
long nLength = sizeof(dwArray)/sizeof(DWORD);
VARIANT varArray[nLength];
HRESULT hr = ADsBuildVarArrayInt(dwArray, nLength, varArray);
if (hr = E_FAIL) exit(1);
 
// Resume work with the data in varArray.
. . .</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>



<a href="https://msdn.microsoft.com/4f0e90e2-afcc-4cf7-a731-9b38a83ca229">ADSI Functions</a>



<a href="https://msdn.microsoft.com/7258a840-691a-4d9b-ab33-bcdf30fd1331">ADsBuildVarArrayStr</a>
 

 

