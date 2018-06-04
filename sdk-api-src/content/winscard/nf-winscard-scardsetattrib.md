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

# SCardSetAttrib function


## -description


The <b>SCardSetAttrib</b> function sets the given <a href="https://msdn.microsoft.com/ce589e18-02ac-42c2-b76b-776deb686bbd">reader</a> attribute for the given handle. It does not affect the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">state</a> of the <a href="https://msdn.microsoft.com/ce589e18-02ac-42c2-b76b-776deb686bbd">reader</a>, <a href="https://msdn.microsoft.com/ce589e18-02ac-42c2-b76b-776deb686bbd">reader driver</a>, or <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">smart card</a>. Not all attributes are supported by all readers (nor can they be set at all times) as many of the attributes are under direct control of the transport protocol.


## -parameters




### -param hCard [in]

Reference value returned from 
<a href="https://msdn.microsoft.com/389ada98-383f-4b37-bf5d-c40577ef25fd">SCardConnect</a>.


### -param dwAttrId [in]

Identifier for the attribute to set. The values are write-only. Note that vendors may not support all attributes. 




					

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SCARD_ATTR_SUPRESS_T1_IFS_REQUEST"></a><a id="scard_attr_supress_t1_ifs_request"></a><dl>
<dt><b>SCARD_ATTR_SUPRESS_T1_IFS_REQUEST</b></dt>
</dl>
</td>
<td width="60%">
Suppress sending of <a href="https://msdn.microsoft.com/11f2e098-1d1e-473b-90ff-7b86eb923e9f">T=1</a> IFSD packet from the reader to the card. (Can be used if the currently inserted card does not support an IFSD request.)

</td>
</tr>
</table>
 


### -param pbAttr [in]

Pointer to a buffer that supplies the attribute whose ID is supplied in <i>dwAttrId</i>.


### -param cbAttrLen [in]

Length (in bytes) of the attribute value in the <i>pbAttr</i> buffer.


## -returns



This function returns different values depending on whether it succeeds or fails.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Success</b></dt>
</dl>
</td>
<td width="60%">
SCARD_S_SUCCESS.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Failure</b></dt>
</dl>
</td>
<td width="60%">
An error code. For more information, see 
<a href="authentication_return_values.htm">Smart Card Return Values</a>.

</td>
</tr>
</table>
 




## -remarks



The <b>SCardSetAttrib</b> function is a direct card access function. For information about other direct access functions, see 
<a href="https://msdn.microsoft.com/ea6cfa5a-2abf-4b7f-b3f4-99655266f030">Direct Card Access Functions</a>.


#### Examples

The following example  shows how to set an attribute.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// Set the attribute.
// hCardHandle was set by a previous call to SCardConnect.
// dwAttrID is a DWORD value, specifying the attribute ID.
// pbAttr points to the buffer of the new value.
// cByte is the count of bytes in the buffer.
lReturn = SCardSetAttrib(hCardHandle,
                         dwAttrID,
                         (LPBYTE)pbAttr,
                         cByte);
if ( SCARD_S_SUCCESS != lReturn )
    printf("Failed SCardSetAttrib\n");
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/389ada98-383f-4b37-bf5d-c40577ef25fd">SCardConnect</a>



<a href="https://msdn.microsoft.com/309ac107-175b-489e-b428-b87bc4204f34">SCardGetAttrib</a>
 

 

