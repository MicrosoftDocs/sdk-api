---
UID: NF:certpol.ICertPolicy.ShutDown
title: ICertPolicy::ShutDown
author: windows-driver-content
description: Called by the server engine before the server is terminated.
old-location: security\icertpolicy2_shutdown.htm
old-project: SecCrypto
ms.assetid: 2a796acb-b179-4b6f-8864-9e96f4049389
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: CCertPolicy object [Security],ShutDown method, ICertPolicy interface [Security],ShutDown method, ICertPolicy.ShutDown, ICertPolicy2 interface [Security],ShutDown method, ICertPolicy2::ShutDown, ICertPolicy::ShutDown, ShutDown, ShutDown method [Security], ShutDown method [Security],CCertPolicy object, ShutDown method [Security],ICertPolicy interface, ShutDown method [Security],ICertPolicy2 interface, _certsrv_icertpolicy_shutdown, certpol/ICertPolicy2::ShutDown, certpol/ICertPolicy::ShutDown, security.icertpolicy2_shutdown
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
req.typenames: X509SCEPFailInfo
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Certidl.lib
-	Certidl.dll
api_name:
-	ICertPolicy2.ShutDown
-	ICertPolicy.ShutDown
-	CCertPolicy.ShutDown
product: Windows
targetos: Windows
req.lib: Certidl.lib
req.dll: 
req.irql: 
---

# ICertPolicy::ShutDown


## -description


The <b>ShutDown</b> method is called by the server engine before the server is terminated.

When <b>ShutDown</b> is called, the policy module should clean up and stop. It is guaranteed that no requests will arrive after <b>ShutDown</b> is called.


## -parameters






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
#include &lt;stdio.h&gt;
#include &lt;Certpol.h&gt;

STDMETHODIMP CCertPolicy::ShutDown()
{
    // Clean up resources used by this process.

    // Display message that this method has been called.
    if ( fDebug )
    {
        printf("Policy module Shutdown was called\n");
    }
    return( S_OK );
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/14031490-be8e-47f9-8c66-ae27f7d3599c">ICertPolicy</a>



<a href="https://msdn.microsoft.com/2e48b096-e23a-4106-bfaf-f089d2291fba">ICertPolicy2</a>
 

 

