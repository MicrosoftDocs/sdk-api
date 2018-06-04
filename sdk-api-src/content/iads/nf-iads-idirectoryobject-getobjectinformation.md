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

# IDirectoryObject::GetObjectInformation


## -description


The <b>IDirectoryObject::GetObjectInformation</b> method retrieves a pointer to an <a href="https://msdn.microsoft.com/f072b2f8-8c03-4f90-8edf-cf5fed97a222">ADS_OBJECT_INFO</a> structure that contains data regarding the identity and location of a directory service object.


## -parameters




### -param ppObjInfo [out]

Provides the address of a pointer to an  <a href="https://msdn.microsoft.com/f072b2f8-8c03-4f90-8edf-cf5fed97a222">ADS_OBJECT_INFO</a> structure that contains data regarding the requested directory service object. If <i>ppObjInfo</i> is <b>NULL</b> on return, <b>GetObjectInformation</b> cannot obtain the requested data.


## -returns



This method returns the standard return values, including <b>S_OK</b> when the data is obtained successfully. For more information and other return values, see  <a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>.




## -remarks



The caller should call 
the <a href="https://msdn.microsoft.com/e43f050a-5b96-406e-87ed-88a39ea747da">FreeADsMem</a> helper function to release the  <a href="https://msdn.microsoft.com/f072b2f8-8c03-4f90-8edf-cf5fed97a222">ADS_OBJECT_INFO</a> structure created by the  <b>GetObjectInformation</b> function.

Automation clients must call  <a href="https://msdn.microsoft.com/73ceaeb1-9a6b-449a-9851-3756736dbad7">IADs::GetInfo</a>.


#### Examples

The following C++ code example shows how to retrieve the object data (<a href="https://msdn.microsoft.com/f072b2f8-8c03-4f90-8edf-cf5fed97a222">ADS_OBJECT_INFO</a>) using the <b>GetObjectInformation</b> method of an object (m_pDirObject) that implements the  <a href="https://msdn.microsoft.com/bc4f8920-2881-4393-bb01-ed837c3db6ad">IDirectoryObject</a> interface.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>ADS_OBJECT_INFO *pInfo;
HRESULT hr;
 
hr = m_pDirObject-&gt;GetObjectInformation(&amp;pInfo);
if (!SUCCEEDED(hr) )
{
   return;
}
 
//////////////////////////
// Show the attributes 
/////////////////////////
 
printf("RDN: %S\n", pInfo-&gt;pszRDN);
printf("ObjectDN: %S\n", pInfo-&gt;pszObjectDN);
printf("Parent DN: %S\n", pInfo-&gt;pszParentDN);
printf("Class Name: %S\n", pInfo-&gt;pszClassName);
printf("Schema DN: %S\n", pInfo-&gt;pszSchemaDN);
 
///////////////////////////////////////////////////////////
// Remember to clean up the memory using FreeADsMem.
//////////////////////////////////////////////////////////
FreeADsMem( pInfo );</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>



<a href="https://msdn.microsoft.com/f072b2f8-8c03-4f90-8edf-cf5fed97a222">ADS_OBJECT_INFO</a>



<a href="https://msdn.microsoft.com/73ceaeb1-9a6b-449a-9851-3756736dbad7">IADs::GetInfo</a>



<a href="https://msdn.microsoft.com/bc4f8920-2881-4393-bb01-ed837c3db6ad">IDirectoryObject</a>
 

 

