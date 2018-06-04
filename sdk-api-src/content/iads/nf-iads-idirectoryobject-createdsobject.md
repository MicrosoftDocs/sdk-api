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

# IDirectoryObject::CreateDSObject


## -description


The <b>IDirectoryObject::CreateDSObject</b> method creates a child of the current directory service object.


## -parameters




### -param pszRDNName [in]

Provides the relative distinguished name (relative path) of the object to be created.


### -param pAttributeEntries [in]

An array of  <a href="https://msdn.microsoft.com/a2b97a52-4b8b-4491-8798-72a161903422">ADS_ATTR_INFO</a> structures that contain attribute definitions to be set when the object is created.


### -param dwNumAttributes [in]

Provides a number of attributes set when the object is created.


### -param ppObject [out]

Provides a pointer to the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface on the created object.


## -returns



This method returns the standard return values, including S_OK for a successful operation. For more information and other return values, see  <a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>.




## -remarks



Specify all attributes to be initialized on creation in the <i>pAttributeEntries</i> array. You may also specify optional attributes. When creating a directory object with this method, attributes with any of the string data types cannot be empty or zero-length.


#### Examples

The following C/C++ code example shows how to create a user object using the <b>IDirectoryObject::CreateDSObject</b> method.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>HRESULT    hr;
IDirectoryObject *pDirObject=NULL;
ADSVALUE   sAMValue;
ADSVALUE   uPNValue;
ADSVALUE   classValue;
LPDISPATCH pDisp;
 
ADS_ATTR_INFO  attrInfo[] = 
{  
   { L"objectClass", ADS_ATTR_UPDATE, 
                       ADSTYPE_CASE_IGNORE_STRING, &amp;classValue, 1 },
   {L"sAMAccountName", ADS_ATTR_UPDATE, 
                       ADSTYPE_CASE_IGNORE_STRING, &amp;sAMValue, 1},
   {L"userPrincipalName", ADS_ATTR_UPDATE, 
                      ADSTYPE_CASE_IGNORE_STRING, &amp;uPNValue, 1},
};
DWORD dwAttrs = sizeof(attrInfo)/sizeof(ADS_ATTR_INFO); 
 
classValue.dwType = ADSTYPE_CASE_IGNORE_STRING;
classValue.CaseIgnoreString = L"user";
 
sAMValue.dwType=ADSTYPE_CASE_IGNORE_STRING;
sAMValue.CaseIgnoreString = L"jeffsmith";
 
uPNValue.dwType=ADSTYPE_CASE_IGNORE_STRING;
uPNValue.CaseIgnoreString = L"jeffsmith@Fabrikam.com";
 
hr = ADsGetObject(L"LDAP://OU=Sales,DC=Fabrikam,DC=com",
          IID_IDirectoryObject, (void**) &amp;pDirObject );
 
if ( SUCCEEDED(hr) )
{
    hr = pDirObject-&gt;CreateDSObject( L"CN=Jeff Smith",  attrInfo, 
                                    dwAttrs, &amp;pDisp );

    if ( SUCCEEDED(hr) )
    {
         // Use the DS object.

         pDisp-&gt;Release();
    }

    pDirObject-&gt;Release();
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>



<a href="https://msdn.microsoft.com/a2b97a52-4b8b-4491-8798-72a161903422">ADS_ATTR_INFO</a>



<a href="https://msdn.microsoft.com/bc4f8920-2881-4393-bb01-ed837c3db6ad">IDirectoryObject</a>
 

 

