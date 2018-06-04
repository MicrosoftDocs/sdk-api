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

# IADsContainer::GetObject


## -description


The <b>IADsContainer::GetObject</b> method retrieves an 
interface for a directory object in the container.


## -parameters




### -param ClassName




### -param RelativeName




### -param ppObject






#### - bstrClassName [in]

A <b>BSTR</b> that specifies the name of the object class as of the object to retrieve. If this parameter is <b>NULL</b>, the provider returns the first item found in the container.


#### - bstrRelativeName [in]

A <b>BSTR</b> that specifies the relative distinguished name of the object to retrieve.


#### - ppNamedObject [out]

A pointer to a pointer to the  <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface on the specified object.


## -returns



This method supports standard return values, including S_OK for a successful operation. For more information about error codes, see  <a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>.




## -remarks



For the LDAP provider, the <i>bstrRelativeName</i> parameter must contain the name prefix, such as "CN=Jeff Smith". The <i>bstrRelativeName</i> parameter can also contain more than one level of name, such as "CN=Jeff Smith,OU=Sales".

In C++, when <b>GetObject</b> has succeeded, the caller must query the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface for the desired interface using the <a href="_com_iunknown_queryinterface">QueryInterface</a> method.

The <i>bstrClassName</i> parameter can be either a valid class name or <b>NULL</b>. If the class name is not valid, including when it contains a blank space, this method will throw an <a href="https://msdn.microsoft.com/193c5808-fc39-48e6-8bb8-8338e5c980ad">E_ADS_UNKNOWN_OBJECT</a> error.


#### Examples

The following code example  retrieves a user object from a container object.

<div class="code"><span codelanguage="VisualBasic"><table>
<tr>
<th>VB</th>
</tr>
<tr>
<td>
<pre>Dim cont As IADsContainer
Dim usr As IADsUser
Set cont = GetObject("LDAP://OU=Sales,DC=Fabrikam,DC=com")
Set usr = cont.GetObject("user", "CN=jeffsmith")</pre>
</td>
</tr>
</table></span></div>
This is equivalent to:

<div class="code"><span codelanguage="VisualBasic"><table>
<tr>
<th>VB</th>
</tr>
<tr>
<td>
<pre>Dim usr As IADsUser
Set usr=GetObject("LDAP://CN=jeffsmith,OU=Sales,DC=Fabrikam,DC=com")</pre>
</td>
</tr>
</table></span></div>
The following code example retrieves a user object from a container object.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>HRESULT hr = S_OK;
CoInitialize(NULL);
 
IADsContainer *pCont = NULL;
 
hr = ADsGetObject(L"LDAP://DC=windows2000,DC=mytest,DC=fabrikam,DC=com",
            IID_IADsContainer, 
            (void**) &amp;pCont );

if(FAILED(hr))
{
    goto Cleanup;
}
 
///////////////////////////////////////////////////////////////////////
// Retrieve the child from the container.
// Be aware that in the LDAP provider you can navigate multiple levels.
///////////////////////////////////////////////////////////////////////
IDispatch *pDisp = NULL;
IADs *pADs = NULL;
hr = pCont-&gt;GetObject(CComBSTR("user"), CComBSTR("CN=Jeff Smith,OU=DSys"), &amp;pDisp);
pCont-&gt;Release();
if(FAILED(hr))
{
    goto Cleanup;
}
 
hr = pDisp-&gt;QueryInterface(IID_IADs, (void**)&amp;pADs);
pDisp-&gt;Release(); 
if(FAILED(hr))
{
    goto Cleanup;
}
 
// Perform an operation with pADs.
pADs-&gt;Release();
 
Cleanup:
if(pCont)
    pCont-&gt;Release();

if(pDisp)
    pDisp-&gt;Release();

if(pADs)
    pADs-&gt;Release();

CoUninitialize();</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error
  Codes</a>



<a href="https://msdn.microsoft.com/595b2c7f-584c-4343-a75c-327d8ed4ceb1">ADsGetObject</a>



<a href="https://msdn.microsoft.com/f53d9ee0-3f4d-4a01-b953-98d168ad94cb">IADs</a>



<b>IADs::get_Class</b>



<b>IADs::get_Name</b>



<a href="https://msdn.microsoft.com/6c1d6c7c-e003-47f9-adfa-4a753fb3e9b2">IADsContainer</a>



<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>
 

 

