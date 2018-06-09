---
UID: NF:certmod.ICertManageModule.GetProperty
title: ICertManageModule::GetProperty
author: windows-sdk-content
description: Retrieves a module's property value.
old-location: security\icertmanagemodule_getproperty.htm
old-project: SecCrypto
ms.assetid: f01bfcec-7031-4283-a847-0d59929e4ee5
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: CCertManageModule object [Security],GetProperty method, Copyright, Description, File Version, GetProperty, GetProperty method [Security], GetProperty method [Security],CCertManageModule object, GetProperty method [Security],ICertManageModule interface, ICertManageModule interface [Security],GetProperty method, ICertManageModule.GetProperty, ICertManageModule::GetProperty, Name, Product Version, _certsrv_icertmanagemodule_getproperty, certmod/ICertManageModule::GetProperty, security.icertmanagemodule_getproperty
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: certmod.h
req.include-header: Certsrv.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: X509RequestType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certidl.lib
 - Certidl.dll
api_name:
 - ICertManageModule.GetProperty
 - CCertManageModule.GetProperty
product: Windows
targetos: Windows
req.lib: Certidl.lib
req.dll: 
req.irql: 
---

# ICertManageModule::GetProperty


## -description


The <b>GetProperty</b> method retrieves a module's property value.


## -parameters




### -param strConfig [in]

Represents the configuration string for the Certificate Services server in the form COMPUTERNAME\CANAME, where COMPUTERNAME is the Certificate Services server's network name, and CANAME is the common name of the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certification authority</a> (CA) as entered for the CA during Certificate Services setup. For information about the configuration string name, see 
<a href="https://msdn.microsoft.com/92bece6a-73f0-47cf-8142-77e986448824">ICertConfig</a>.


### -param strStorageLocation [in]

A registry key that denotes the storage location in the <b>HKEY_LOCAL_MACHINE</b> hive for the property values. This value is in the following form:


<pre xml:space="preserve"><b>SYSTEM</b>
   <b>CurrentControlSet</b>
      <b>Services</b>
         <b>CertSvc</b>
            <b>Configuration</b>
               <i>CAName</i>
                  <i>PolicyOrExitModules</i>
                     <i>MyModule.PolicyOrExit</i></pre>


The <i>CAName</i> is the name of the certification authority's configuration string, <i>PolicyOrExitModules</i> will be either "Policy" or "Exit" (depending on whether a Policy or Exit module applies to this implementation of <b>ICertManageModule</b>), and <i>MyModule.PolicyOrExit</i> is the application-specific identifier for the module. Note that <i>CAName</i> is the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">sanitized name</a> for the certification authority. For information about the sanitized name, see 
<a href="https://msdn.microsoft.com/3a35b2a0-f8e4-496d-b76a-a7310842cc4c">ICertConfig::GetConfig</a>. The use of this storage location is for future use.


### -param strPropertyName [in]

The name of the property being queried. Policy and exit modules should support the following properties. 




					

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="Name"></a><a id="name"></a><a id="NAME"></a><dl>
<dt><b>Name</b></dt>
</dl>
</td>
<td width="60%">
Name of the module.

</td>
</tr>
<tr>
<td width="40%"><a id="Description"></a><a id="description"></a><a id="DESCRIPTION"></a><dl>
<dt><b>Description</b></dt>
</dl>
</td>
<td width="60%">
Description of the module.

</td>
</tr>
<tr>
<td width="40%"><a id="Copyright"></a><a id="copyright"></a><a id="COPYRIGHT"></a><dl>
<dt><b>Copyright</b></dt>
</dl>
</td>
<td width="60%">
Copyright pertaining to the module.

</td>
</tr>
<tr>
<td width="40%"><a id="File_Version"></a><a id="file_version"></a><a id="FILE_VERSION"></a><dl>
<dt><b>File Version</b></dt>
</dl>
</td>
<td width="60%">
Version of the module file.

</td>
</tr>
<tr>
<td width="40%"><a id="Product_Version"></a><a id="product_version"></a><a id="PRODUCT_VERSION"></a><dl>
<dt><b>Product Version</b></dt>
</dl>
</td>
<td width="60%">
Version of the module.

</td>
</tr>
</table>
 


### -param Flags [in]

This parameter is reserved and must be set to zero.


### -param pvarProperty [out, retval]

A pointer to a <b>VARIANT</b> that is the retrieved value for the property specified by <i>strPropertyName</i>.


## -returns



<h3>C++</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.

<h3>VB</h3>
 The return value is a <b>Variant</b> that represents the value of the property named <i>strPropertyName</i>.




## -remarks



Implementing <b>ICertManageModule</b> allows the Certificate Services Manager to retrieve the module's properties by calling <b>GetProperty</b>. The properties can then be displayed in Certificate Services Manager property pages for Policy and Exit Modules. The Certificate Services Manager will pass the location referenced by <i>strStorageLocation</i> to this module, and in future versions the implementation of this method can then use this location as needed. The following example does not use <i>strStorageLocation</i> but instead, maintains the property values in memory.


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#include &lt;windows.h&gt;
#include &lt;Certmod.h&gt;

HRESULT CCertManagePolicyModule::GetProperty(
            /* [in] */ const BSTR strConfig,
            /* [in] */ BSTR strStorageLocation,
            /* [in] */ BSTR strPropertyName,
            /* [in] */ LONG Flags,
            /* [retval][out] */ VARIANT *pvarProperty)
{
    // Array of property Names.
    // These values are defined in Certmod.h.
    wchar_t const * awszPropName[] =
    {
        wszCMM_PROP_NAME,
        wszCMM_PROP_DESCRIPTION,
        wszCMM_PROP_COPYRIGHT,
        wszCMM_PROP_FILEVER,
        wszCMM_PROP_PRODUCTVER
    };

    // Array of property Values.
    // These values are module-specific, and
    // correspond to the property names in    
    // awszPropName (same index).
    wchar_t const * awszPropValue[] = 
   {
        L"MyModule",                      // NAME
        L"Description of MyModule",       // DESCRIPTION
        L"Copyright 1998",                // COPYRIGHT
        L"1.0",                           // FILE VERSION
        L"1.0"                            // PRODUCT VERSION
    };
    int     i;
    bool    bFound = FALSE;
    HRESULT hr;

    // Return appropriate error if strPropertyName is NULL.
    if (NULL == strPropertyName)
        return E_INVALIDARG;

    // Return appropriate error if pvarProperty is NULL.
    if (NULL == pvarProperty)
        return E_POINTER;
    // Determine whether the requested property is in the Name array.
    for (i=0; i&lt;sizeof(awszPropName)/sizeof(wchar_t *); i++)
        if (!wcscmp( strPropertyName, awszPropName[i]))        
        {
            bFound = TRUE;  // Found the index for the property.
            break;
        }
    if ( !bFound )
        return S_FALSE;     // Requested property not found.

    // Allocate storage for the property value.
    pvarProperty-&gt;bstrVal = SysAllocString(awszPropValue[i]);
    if (NULL == pvarProperty-&gt;bstrVal)
        return E_OUTOFMEMORY;   

    pvarProperty-&gt;vt = VT_BSTR;

    return S_OK;
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<b>CCertManageModule</b>



<a href="https://msdn.microsoft.com/92bece6a-73f0-47cf-8142-77e986448824">ICertConfig</a>



<a href="https://msdn.microsoft.com/82b7b770-c098-40da-8a4e-8eb0e0b8a645">ICertManageModule</a>



<a href="https://msdn.microsoft.com/582ace4a-da88-41b7-86dd-d6a74fc9e97a">ICertManageModule::SetProperty</a>
 

 

