---
UID: NE:iads.__MIDL___MIDL_itf_ads_0001_0017_0001
title: ADS_SYSTEMFLAG_ENUM
author: windows-sdk-content
description: The ADS_SYSTEMFLAG_ENUM enumeration defines some of the values that can be assigned to the systemFlags attribute. Some of the values in the enumeration are specific to attributeSchema objects; other values can be set on objects of any class.
old-location: adsi\ads_systemflag_enum.htm
tech.root: adsi
ms.assetid: 7b77bcf0-8db9-4b27-96a4-953a4fa426f5
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ADS_SYSTEMFLAG_ATTR_IS_CONSTRUCTED, ADS_SYSTEMFLAG_ATTR_NOT_REPLICATED, ADS_SYSTEMFLAG_CONFIG_ALLOW_LIMITED_MOVE, ADS_SYSTEMFLAG_CONFIG_ALLOW_MOVE, ADS_SYSTEMFLAG_CONFIG_ALLOW_RENAME, ADS_SYSTEMFLAG_CR_NTDS_DOMAIN, ADS_SYSTEMFLAG_CR_NTDS_NC, ADS_SYSTEMFLAG_DISALLOW_DELETE, ADS_SYSTEMFLAG_DOMAIN_DISALLOW_MOVE, ADS_SYSTEMFLAG_DOMAIN_DISALLOW_RENAME, ADS_SYSTEMFLAG_ENUM, ADS_SYSTEMFLAG_ENUM enumeration [ADSI], _ds_ads_systemflag_enum, adsi.ads__systemflag__enum, adsi.ads_systemflag_enum, iads/ADS_SYSTEMFLAG_ATTR_IS_CONSTRUCTED, iads/ADS_SYSTEMFLAG_ATTR_NOT_REPLICATED, iads/ADS_SYSTEMFLAG_CONFIG_ALLOW_LIMITED_MOVE, iads/ADS_SYSTEMFLAG_CONFIG_ALLOW_MOVE, iads/ADS_SYSTEMFLAG_CONFIG_ALLOW_RENAME, iads/ADS_SYSTEMFLAG_CR_NTDS_DOMAIN, iads/ADS_SYSTEMFLAG_CR_NTDS_NC, iads/ADS_SYSTEMFLAG_DISALLOW_DELETE, iads/ADS_SYSTEMFLAG_DOMAIN_DISALLOW_MOVE, iads/ADS_SYSTEMFLAG_DOMAIN_DISALLOW_RENAME, iads/ADS_SYSTEMFLAG_ENUM
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Iads.h
api_name:
 - ADS_SYSTEMFLAG_ENUM
product: Windows
targetos: Windows
req.typenames: ADS_SYSTEMFLAG_ENUM
req.redist: 
---

# ADS_SYSTEMFLAG_ENUM enumeration


## -description


The <b>ADS_SYSTEMFLAG_ENUM</b> enumeration defines some of the values that can be assigned to the <b>systemFlags</b> attribute. Some of the values in the enumeration are specific to <b>attributeSchema</b> objects; other values can be set on objects of any class.


## -enum-fields




### -field ADS_SYSTEMFLAG_DISALLOW_DELETE

Identifies an object that cannot be deleted.


### -field ADS_SYSTEMFLAG_CONFIG_ALLOW_RENAME

For objects in the configuration partition, if this flag is set, the object can be renamed; otherwise, the object cannot be renamed. By default, this flag is not set on new objects created under the configuration partition, and you can set this flag only during object creation.


### -field ADS_SYSTEMFLAG_CONFIG_ALLOW_MOVE

For objects in the configuration partition, if this flag is set, the object can be moved; otherwise, the object cannot be moved. By default, this flag is not set on new objects created under the configuration partition, and you can set this flag only during object creation.


### -field ADS_SYSTEMFLAG_CONFIG_ALLOW_LIMITED_MOVE

For objects in the configuration partition, if this flag is set, the object can be moved with restrictions; otherwise, the object cannot be moved. By default, this flag is not set on new objects created under the configuration partition, and you can set this flag only during object creation.


### -field ADS_SYSTEMFLAG_DOMAIN_DISALLOW_RENAME

Identifies a domain object that cannot be renamed.


### -field ADS_SYSTEMFLAG_DOMAIN_DISALLOW_MOVE

Identifies a domain object that cannot be moved.


### -field ADS_SYSTEMFLAG_CR_NTDS_NC

Naming context is in NTDS.


### -field ADS_SYSTEMFLAG_CR_NTDS_DOMAIN

Naming context is a domain.


### -field ADS_SYSTEMFLAG_ATTR_NOT_REPLICATED

If this flag is set in the <b>systemFlags</b> attribute of an <b>attributeSchema</b> object, the attribute is not to be replicated.


### -field ADS_SYSTEMFLAG_ATTR_IS_CONSTRUCTED

If this flag is set in the <b>systemFlags</b> attribute of an <b>attributeSchema</b> object, the attribute is a constructed property.


## -remarks



For <b>classSchema</b> and <b>attributeSchema</b> objects, the 0x10 bit of the <b>systemFlags</b> attribute indicates an object that is part of the base schema included with Active Directory. This bit cannot be set on new <b>classSchema</b> and <b>attributeSchema</b> objects. The <b>ADS_SYSTEMFLAG_ENUM</b> enumeration does not include a constant for this bit.

<div class="alert"><b>Note</b>  Because VBScript cannot read data from a type library, VBScript applications do not recognize the symbolic constants as defined above. Use the numeric constants instead to set the appropriate flags in your VBScript applications. To use the symbolic constants as a good programming practice, you should make explicit declarations of such constants, as done here, in your VBScript applications.</div>
<div> </div>

#### Examples

The following code example shows how elements of the <b>ADS_SYSTEMFLAG_ENUM</b> enumeration, together with the  <a href="https://msdn.microsoft.com/e8989795-8f72-476a-a69e-c0e8800289ab">IDirectorySearch</a> interface, are used to search non-replicated properties.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#include &lt;wchar.h&gt;
#include &lt;activeds.h&gt;
#include &lt;atlbase.h&gt;
 
HRESULT hr = E_FAIL;
LPWSTR szPrefix = L"LDAP://%s";
LPWSTR szPath = NULL;
IDirectorySearch *pSchemaNC = NULL;
IADs *pObject = NULL;
size_t nLength = 0;
LPWSTR pszSearchFilterTemplate = L"(&amp;(objectCategory=attributeSchema)(systemFlags:1.2.840.113556.1.4.804:=%d))";
LPWSTR pszSearchFilter = NULL;
 
CoInitialize(NULL);     // Initialize COM

// Get rootDSE and the schema container distinguished name.
// Bind to current user's domain using current user's security context.
hr = ADsOpenObject(L"LDAP://rootDSE",
                NULL,
                NULL,
                ADS_SECURE_AUTHENTICATION, // Use Secure Authentication.
                IID_IADs,
                (void**)&amp;pObject);
if (SUCCEEDED(hr))
{
    CComVarinat svar;
    hr = pObject-&gt;Get(CComBSTR("schemaNamingContext"), &amp;svar);
    if (SUCCEEDED(hr))
    {
        nLength = wcslen(szPrefix) + wcslen(svar.bstrVal) + 1;
        szPath = new WCHAR[nLength];
        swprintf_s(szPath, szPrefix, svar.bstrVal);

        hr = ADsOpenObject(szPath,
            NULL,
            NULL,
            ADS_SECURE_AUTHENTICATION, 
            IID_IDirectorySearch,
            (void**)&amp;pSchemaNC);

        delete [] szPath;

        if (SUCCEEDED(hr))
        {
            wprintf(L"Find non-replicated attributes\n");
 
            // Create search filter to find attributes with systemFlags that 
            // match ADS_SYSTEMFLAG_ATTR_NOT_REPLICATED
            nLength = wcslen(pszSearchFilterTemplate) + 25 + 1;
            pszSearchFilter = new WCHAR[nLength];
            swprintf_s(pszSearchFilter, pszSearchFilterTemplate, ADS_SYSTEMFLAG_ATTR_NOT_REPLICATED);
     
            // Attributes are one-level deep in the schema container 
            // so only need to search one level.
            ADS_SEARCHPREF_INFO SearchPrefs;
            SearchPrefs.dwSearchPref = ADS_SEARCHPREF_SEARCH_SCOPE;
            SearchPrefs.vValue.dwType = ADSTYPE_INTEGER;
            SearchPrefs.vValue.Integer = ADS_SCOPE_ONELEVEL;
            DWORD dwNumPrefs = 1;
     
            // COL for iterations.
            ADS_SEARCH_COLUMN    col;
     
            // Handle used for searching.
            ADS_SEARCH_HANDLE hSearch;
     
            IADs    *pObj = NULL;
            IADs    * pIADs = NULL;
 
            // Set the search preference.
            hr = pSchemaNC-&gt;SetSearchPreference( &amp;SearchPrefs, dwNumPrefs);
            if (FAILED(hr)) 
            {
                return hr;
            }
 
            CONST DWORD dwAttrNameSize = 1;
            LPOLESTR pszAttribute[dwAttrNameSize];
            pszAttribute[0] = L"cn";

            // Execute the search.
            hr = pSchemaNC-&gt;ExecuteSearch(pszSearchFilter,
                                          pszAttribute,
                                          dwAttrNameSize,
                                          &amp;hSearch );

            delete [] pszSearchFilter;
            if ( SUCCEEDED(hr) ) 
            { 
                // Call IDirectorySearch::GetNextRow() to retrieve 
                // the next row of data.
                while( pSchemaNC-&gt;GetNextRow( hSearch) != S_ADS_NOMORE_ROWS) 
                {
                    // Loop through the array of passed column names,
                    // print the data for each column.
                    for (DWORD x = 0; x &lt; dwAttrNameSize; x++) 
                    {
                        // Get the data for this column.
                        hr = pSchemaNC-&gt;GetColumn( hSearch, 
                                           pszAttribute[x], 
                                           &amp;col );
                        if ( SUCCEEDED(hr) ) 
                        {
                            // Print the data for the column and 
                            // free the column.
                            if (col.dwADsType == ADSTYPE_CASE_IGNORE_STRING)
                            {
                                wprintf(L"%s: %s\r\n", 
                                pszAttribute[x], 
                                col.pADsValues-&gt;CaseIgnoreString); 
                            }
                            else
                            {
                                wprintf(L"&lt;%s property is not a string&gt;", pszAttribute[x]);
                            }

                            pSchemaNC-&gt;FreeColumn( &amp;col );
                        }
                    }
                }

                // Close the search handle to clean up.
                pSchemaNC-&gt;CloseSearchHandle(hSearch);
            } 
        }
    } 

    pObject-&gt;Release();
}

CoUninitialize();    // uninitialize COM.
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/f0ad5ce5-742d-40dc-ac5a-31d779e40bfd">ADSI
  Enumerations</a>



<a href="https://msdn.microsoft.com/e8989795-8f72-476a-a69e-c0e8800289ab">IDirectorySearch</a>
 

 

