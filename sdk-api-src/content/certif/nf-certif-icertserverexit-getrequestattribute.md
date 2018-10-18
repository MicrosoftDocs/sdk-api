---
UID: NF:certif.ICertServerExit.GetRequestAttribute
title: ICertServerExit::GetRequestAttribute
author: windows-sdk-content
description: Returns a named attribute value from a request.
old-location: security\icertserverexit_getrequestattribute.htm
tech.root: seccrypto
ms.assetid: 894bde77-5e76-452b-acf5-c73fcaf1fa31
ms.author: windowssdkdev
ms.date: 10/17/2018
ms.keywords: CCertServerExit object [Security],GetRequestAttribute method, GetRequestAttribute, GetRequestAttribute method [Security], GetRequestAttribute method [Security],CCertServerExit object, GetRequestAttribute method [Security],ICertServerExit interface, ICertServerExit interface [Security],GetRequestAttribute method, ICertServerExit.GetRequestAttribute, ICertServerExit::GetRequestAttribute, _certsrv_icertserverexit_getrequestattribute, certif/ICertServerExit::GetRequestAttribute, security.icertserverexit_getrequestattribute
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: certif.h
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
req.lib: Certidl.lib
req.dll: Certcli.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certcli.dll
api_name:
 - ICertServerExit.GetRequestAttribute
 - CCertServerExit.GetRequestAttribute
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICertServerExit::GetRequestAttribute


## -description


The <b>GetRequestAttribute</b> method returns a named <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">attribute</a> value from a request.

Prior to calling this method, it is necessary to call 
<a href="https://msdn.microsoft.com/8d317114-17bd-4b22-8e37-99db72740538">ICertServerExit::SetContext</a>.


## -parameters




### -param strAttributeName [in]

The name of the attribute to retrieve.


### -param pstrAttributeValue [out]

A pointer to a <b>BSTR</b> value that will contain the attribute value.


## -returns



<h3>C++</h3>
If the method succeeds, the method returns S_OK, and *<i>pstrAttributeValue</i> is set to the <b>BSTR</b> that contains the attribute value.

To use this method, create a variable of type <b>BSTR</b>, set the variable equal to <b>NULL</b>, and pass the address of this variable as <i>pstrAttributeValue</i>.

 When you have finished using the <b>BSTR</b>, free it by calling the <a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a> function.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.

<h3>VB</h3>
 The return value is a string that represents the attribute value.




## -remarks



You must call 
<a href="https://msdn.microsoft.com/8d317114-17bd-4b22-8e37-99db72740538">ICertServerExit::SetContext</a> prior to using this method.

The following request attributes are unique to KEYGEN style requests.

<table>
<tr>
<th>Property name</th>
<th>Type</th>
<th>Description</th>
</tr>
<tr>
<td>Challenge</td>
<td><b>String</b></td>
<td>Challenge string that accompanies the request.</td>
</tr>
<tr>
<td>ExpectedChallenge</td>
<td><b>String</b></td>
<td>If the challenge string is incorrect, then the server will set the value of this request attribute to the expected challenge so that failure can be diagnosed.</td>
</tr>
</table>
 


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>BSTR       bstrAttribValue = NULL;
HRESULT    hr;

// Get the request attribute.
// bstrAttribName is a BSTR assigned by EnumerateAttributes.
// Also, ICertServerExit::SetContext has already been
// called by pCertServerExit.
hr = pCertServerExit-&gt;GetRequestAttribute(bstrAttribName,
                                          &amp;bstrAttribValue);

if (FAILED(hr))
{
    printf("Failed GetRequestAttribute [%x]\n", hr);
    goto error;
}
else
{

    // Successful call. Use bstrAttribValue as needed.
    // ...
}

// Done processing. Free BSTR.
if (NULL != bstrAttribValue)
    SysFreeString(bstrAttribValue);</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/1554c09c-a7c1-44ad-9821-93c0913212fc">ICertServerExit</a>



<a href="https://msdn.microsoft.com/8d317114-17bd-4b22-8e37-99db72740538">ICertServerExit::SetContext</a>
 

 

