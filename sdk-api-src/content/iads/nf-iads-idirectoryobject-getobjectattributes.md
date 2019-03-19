---
UID: NF:iads.IDirectoryObject.GetObjectAttributes
title: IDirectoryObject::GetObjectAttributes (iads.h)
author: windows-sdk-content
description: Retrieves one or more specified attributes of the directory service object.
old-location: adsi\idirectoryobject_getobjectattributes.htm
tech.root: adsi
ms.assetid: 6e3d046f-eac0-4955-925b-71ab15df9ed3
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetObjectAttributes, GetObjectAttributes method [ADSI], GetObjectAttributes method [ADSI],IDirectoryObject interface, IDirectoryObject interface [ADSI],GetObjectAttributes method, IDirectoryObject.GetObjectAttributes, IDirectoryObject::GetObjectAttributes, _ds_idirectoryobject_getobjectattributes, adsi.idirectoryobject__getobjectattributes, adsi.idirectoryobject_getobjectattributes, iads/IDirectoryObject::GetObjectAttributes
ms.topic: method
req.header: iads.h
req.include-header: 
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
req.lib: 
req.dll: Activeds.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Activeds.dll
api_name:
 - IDirectoryObject.GetObjectAttributes
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirectoryObject::GetObjectAttributes


## -description


The <b>IDirectoryObject::GetObjectAttributes</b> method retrieves one or more specified attributes of the directory service object.


## -parameters




### -param pAttributeNames [in]

Specifies an array of names of the requested attributes. 




To request all of the object's attributes, set <i>pAttributeNames</i> to <b>NULL</b> and set the <i>dwNumberAttributes</i> parameter to (DWORD)-1.


### -param dwNumberAttributes [in]

Specifies the size of the <i>pAttributeNames</i> array. If -1, all of the object's attributes are requested.


### -param ppAttributeEntries [out]

Pointer to a variable that receives a pointer to an array of  <a href="https://msdn.microsoft.com/a2b97a52-4b8b-4491-8798-72a161903422">ADS_ATTR_INFO</a> structures that contain the requested attribute values. If no attributes could be obtained from the directory service object, the returned pointer is <b>NULL</b>.


### -param pdwNumAttributesReturned [out]

Pointer to a <b>DWORD</b> variable that receives the number of attributes retrieved in the <i>ppAttributeEntries</i> array.


## -returns



This method returns the standard values, as well as the following:

For more information and other return values, see  <a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>.




## -remarks



ADSI allocates the memory for the array of <a href="https://msdn.microsoft.com/a2b97a52-4b8b-4491-8798-72a161903422">ADS_ATTR_INFO</a> structures returned in the <i>ppAttributeEntries</i> parameter. The caller must call  <a href="https://msdn.microsoft.com/e43f050a-5b96-406e-87ed-88a39ea747da">FreeADsMem</a> to free the array.

The order of attributes returned in <i>ppAttributeEntries</i> is not necessarily the same as requested in <i>pAttributeNames</i>.

The <b>IDirectoryObject::GetObjectAttributes</b> method attempts to read the schema definition of the requested attributes so it can return the attribute values in the appropriate format in the <a href="https://msdn.microsoft.com/b53c4a14-9965-4025-95bc-37f460ea2bc9">ADSVALUE</a> structures contained in the <a href="https://msdn.microsoft.com/a2b97a52-4b8b-4491-8798-72a161903422">ADS_ATTR_INFO</a> structures. However, <b>GetObjectAttributes</b> can succeed even when the schema definition is not available, in which case the <b>dwADsType</b> member of the <b>ADS_ATTR_INFO</b> structure returns ADSTYPE_PROV_SPECIFIC and the value is returned in an <a href="https://msdn.microsoft.com/45927280-7fb5-49a6-8ecd-f0a6931bed6a">ADS_PROV_SPECIFIC</a> structure. When you process the results of a <b>GetObjectAttributes</b> call, verify <b>dwADsType</b> to ensure that the data was returned in the expected format.


#### Examples

The following code example shows how the <b>IDirectoryObject::GetObjectAttributes</b> method can be used.


```cpp
HRESULT hr;
IDirectoryObject *pDirObject = NULL;
 
hr = ADsGetObject(L"LDAP://CN=Jeff Smith,OU=Sales,DC=Fabrikam,DC=com",
                     IID_IDirectoryObject, 
                     (void**) &pDirObject );
 
if ( SUCCEEDED(hr) )
{
    ADS_ATTR_INFO *pAttrInfo=NULL;
    DWORD dwReturn;
    LPWSTR pAttrNames[]={L"givenName",L"sn", L"otherTelephone" };
    DWORD dwNumAttr=sizeof(pAttrNames)/sizeof(LPWSTR);

    //////////////////////////////////////////////////////
    // Get attribute values requested.
    // Be aware that the order is not necessarily the 
    // same as requested using pAttrNames.
    //////////////////////////////////////////////////////
    hr = pDirObject->GetObjectAttributes( pAttrNames, 
                                        dwNumAttr, 
                                        &pAttrInfo, 
                                        &dwReturn );
     
    if ( SUCCEEDED(hr) )
    {
        for(DWORD idx = 0; idx < dwReturn; idx++ )
        {
            if ( _wcsicmp(pAttrInfo[idx].pszAttrName,L"givenName") == 0 )
            {
                switch (pAttrInfo[idx].dwADsType)
                {
                    case ADSTYPE_CASE_IGNORE_STRING:
                        printf("First Name: %S\n", pAttrInfo[idx].pADsValues->CaseIgnoreString);
                        break;
         
                    case ADSTYPE_PROV_SPECIFIC:
                        printf("First Name: %S\n", pAttrInfo[idx].pADsValues->ProviderSpecific.lpValue);
                        break;
         
                    default:
                        printf("Invalid ADsType: %d\n", pAttrInfo[idx].dwADsType);
                        break;
                }
            }
            else if ( _wcsicmp(pAttrInfo[idx].pszAttrName, L"sn") == 0 )
            {
                switch (pAttrInfo[idx].dwADsType)
                {
                    case ADSTYPE_CASE_IGNORE_STRING:
                        printf("Last Name: %S\n", pAttrInfo[idx].pADsValues->CaseIgnoreString);
                        break;
         
                    case ADSTYPE_PROV_SPECIFIC:
                        printf("Last Name: %S\n", pAttrInfo[idx].pADsValues->ProviderSpecific.lpValue);
                        break;
         
                    default:
                        printf("Invalid ADsType: %d\n", pAttrInfo[idx].dwADsType);
                        break;
                }
            }
            else if ( _wcsicmp(pAttrInfo[idx].pszAttrName, L"otherTelephone") == 0  )
            {   // Print the multi-valued property, "Other Telephones".
                switch (pAttrInfo[idx].dwADsType)
                {
                    case ADSTYPE_CASE_IGNORE_STRING:
                        printf("Other Telephones:");
                        for (DWORD val=0; val < pAttrInfo[idx].dwNumValues; val++) 
                        printf("  %S\n", pAttrInfo[idx].pADsValues[val].CaseIgnoreString);
                        break;
         
                    case ADSTYPE_PROV_SPECIFIC:
                        printf("Other Telephones:");
                        for (DWORD val=0; val < pAttrInfo[idx].dwNumValues; val++) 
                        printf("  %S\n", pAttrInfo[idx].pADsValues[val].CaseIgnoreString);
                        break;
         
                    default:
                        printf("Other Telephones:");
                        for (DWORD val=0; val < pAttrInfo[idx].dwNumValues; val++) 
                        printf("  %S\n", pAttrInfo[idx].pADsValues[val].CaseIgnoreString);
                        break;
                }
            }
        }

        /////////////////////////////////////////////////////////////
        // Use FreeADsMem for all memory obtained from the ADSI call. 
        /////////////////////////////////////////////////////////////
        FreeADsMem( pAttrInfo );
    
    }
 
    pDirObject->Release();
}
```





## -see-also




<a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>



<a href="https://msdn.microsoft.com/a2b97a52-4b8b-4491-8798-72a161903422">ADS_ATTR_INFO</a>



<a href="https://msdn.microsoft.com/e43f050a-5b96-406e-87ed-88a39ea747da">FreeADsMem</a>



<a href="https://msdn.microsoft.com/bc4f8920-2881-4393-bb01-ed837c3db6ad">IDirectoryObject</a>
 

 

