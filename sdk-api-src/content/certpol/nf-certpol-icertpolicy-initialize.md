---
UID: NF:certpol.ICertPolicy.Initialize
title: ICertPolicy::Initialize
author: windows-sdk-content
description: Called by the server engine to allow the policy module to perform initialization tasks.
old-location: security\icertpolicy2_initialize.htm
tech.root: seccrypto
ms.assetid: b0a0e9a6-79ca-4898-bddd-e736552aaf68
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: CCertPolicy object [Security],Initialize method, ICertPolicy interface [Security],Initialize method, ICertPolicy.Initialize, ICertPolicy2 interface [Security],Initialize method, ICertPolicy2::Initialize, ICertPolicy::Initialize, Initialize, Initialize method [Security], Initialize method [Security],CCertPolicy object, Initialize method [Security],ICertPolicy interface, Initialize method [Security],ICertPolicy2 interface, _certsrv_icertpolicy_initialize, certpol/ICertPolicy2::Initialize, certpol/ICertPolicy::Initialize, security.icertpolicy2_initialize, security.icertpolicy_initialize
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: certpol.h
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certidl.lib
 - Certidl.dll
api_name:
 - ICertPolicy2.Initialize
 - ICertPolicy.Initialize
 - CCertPolicy.Initialize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICertPolicy::Initialize


## -description


The <b>Initialize</b> method is called by the server engine to allow the policy module to perform initialization tasks.


## -parameters




### -param strConfig [in]

Represents the name of the certification authority, as entered during Certificate Services setup. For information about the configuration string name, see 
<a href="https://msdn.microsoft.com/6bac5961-f9cc-4859-affa-aa7ed152ebfa">ICertConfig2</a>.


## -returns



<h3>VB</h3>
 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



When you write custom policy modules, implement this method.


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#include &lt;windows.h&gt;
#include &lt;Certpol.h&gt;

STDMETHODIMP CCertPolicy::Initialize(
    /* [in] */ BSTR const strConfig)
{
    // strConfig can be used by the Policy module.
    // Here, it is stored in a BSTR member variable.
    // m_strConfig is an application-defined variable.
    // Call SysFreeString to free m_strConfig when done.
    m_strConfig = SysAllocString( strConfig );
    // Check to determine whether there was enough memory.
    if (NULL == m_strConfig)
        return ( E_OUTOFMEMORY );  // Not enough memory

    return( S_OK );
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/92bece6a-73f0-47cf-8142-77e986448824">ICertConfig</a>



<a href="https://msdn.microsoft.com/14031490-be8e-47f9-8c66-ae27f7d3599c">ICertPolicy</a>



<a href="https://msdn.microsoft.com/2e48b096-e23a-4106-bfaf-f089d2291fba">ICertPolicy2</a>
 

 

