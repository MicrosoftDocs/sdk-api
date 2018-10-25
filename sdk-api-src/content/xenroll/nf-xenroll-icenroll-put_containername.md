---
UID: NF:xenroll.ICEnroll.put_ContainerName
title: ICEnroll::put_ContainerName
author: windows-sdk-content
description: The ContainerName property of ICEnroll4 sets or retrieves the name of the key container to use.
old-location: security\icenroll4_containername.htm
tech.root: seccrypto
ms.assetid: fa863843-8bbc-47c5-9d58-b64fb6703c0a
ms.author: windowssdkdev
ms.date: 10/24/2018
ms.keywords: CEnroll object [Security],ContainerName property, ContainerName property [Security], ContainerName property [Security],CEnroll object, ContainerName property [Security],ICEnroll interface, ContainerName property [Security],ICEnroll2 interface, ContainerName property [Security],ICEnroll3 interface, ContainerName property [Security],ICEnroll4 interface, ICEnroll interface [Security],ContainerName property, ICEnroll.ContainerName, ICEnroll.put_ContainerName, ICEnroll2 interface [Security],ContainerName property, ICEnroll2.ContainerName, ICEnroll2::get_ContainerName, ICEnroll2::put_ContainerName, ICEnroll3 interface [Security],ContainerName property, ICEnroll3.ContainerName, ICEnroll3::get_ContainerName, ICEnroll3::put_ContainerName, ICEnroll4 interface [Security],ContainerName property, ICEnroll4.ContainerName, ICEnroll4::ContainerName, ICEnroll4::get_ContainerName, ICEnroll4::put_ContainerName, ICEnroll::get_ContainerName, ICEnroll::put_ContainerName, put_ContainerName, security.icenroll4_containername, xenroll/ICEnroll2::ContainerName, xenroll/ICEnroll2::get_ContainerName, xenroll/ICEnroll2::put_ContainerName, xenroll/ICEnroll3::ContainerName, xenroll/ICEnroll3::get_ContainerName, xenroll/ICEnroll3::put_ContainerName, xenroll/ICEnroll4::ContainerName, xenroll/ICEnroll4::get_ContainerName, xenroll/ICEnroll4::put_ContainerName, xenroll/ICEnroll::ContainerName, xenroll/ICEnroll::get_ContainerName, xenroll/ICEnroll::put_ContainerName
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: xenroll.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
req.lib: Uuid.lib
req.dll: Xenroll.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Xenroll.dll
api_name:
 - ICEnroll4.ContainerName
 - ICEnroll4.get_ContainerName
 - ICEnroll4.put_ContainerName
 - ICEnroll3.ContainerName
 - ICEnroll3.get_ContainerName
 - ICEnroll3.put_ContainerName
 - ICEnroll2.ContainerName
 - ICEnroll2.get_ContainerName
 - ICEnroll2.put_ContainerName
 - ICEnroll.ContainerName
 - ICEnroll.get_ContainerName
 - ICEnroll.put_ContainerName
 - CEnroll.ContainerName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICEnroll::put_ContainerName


## -description


<p class="CCE_Message">[This property is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>ContainerName</b> property sets or retrieves the  name of the <a href="https://msdn.microsoft.com/f17042c3-ba1a-408f-af55-5f171b0dee33">key container</a> to use.

This property was first defined in the <a href="https://msdn.microsoft.com/d5b746e0-91bd-45bd-9a67-ddc8868cee56">ICEnroll</a> interface.

This property is read/write.


## -parameters


## -remarks



The container specified may be an existing container or a new one. It may only be an existing container if the 
<a href="https://msdn.microsoft.com/e5115033-bda1-4160-84b3-80c692bf64fb">UseExistingKeySet</a> property is set, as long as the key set has not been generated yet. For example, if only an <a href="https://msdn.microsoft.com/f1caccd2-3453-448e-b194-bf899eff8091">exchange key</a> set has been generated for a container, it is still possible to perform a certificate enrollment using the signature key set without setting <b>UseExistingKeySet</b>. The <i>exchange key set</i> could be used if <b>UseExistingKeySet</b> is set beforehand.

By default, a new container is selected each time the <a href="https://msdn.microsoft.com/d5b746e0-91bd-45bd-9a67-ddc8868cee56">ICEnroll</a> control is run. This ensures that a new key set is generated. If this property is not explicitly set, a generated GUID is used as the container name.


The <b>ContainerName</b> property affects the behavior of the following methods:

<ul>
<li>
<a href="https://msdn.microsoft.com/b8e841c1-f16e-4f3a-94f2-ef6708c88910">createPKCS10</a>
</li>
<li>
<a href="https://msdn.microsoft.com/074c7321-6117-4261-836a-a2055c9e029d">createFilePKCS10</a>
</li>
</ul>



#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>BSTR     bstrContainerName = NULL;
HRESULT  hr;

// pEnroll is previously instantiated ICEnroll interface pointer

// get the container name
hr = pEnroll-&gt;get_ContainerName( &amp;bstrContainerName );
if ( FAILED ( hr ) )
    printf("Failed getting ContainerName - %x\n", hr );
else
    printf( "ContainerName: %ws\n", bstrContainerName );
// free BSTR when done
if ( NULL != bstrContainerName )
    SysFreeString( bstrContainerName );

// set the container name
// bstrMyName previously set to a valid name
hr = pEnroll-&gt;put_ContainerName( bstrMyName );
if ( FAILED ( hr ) )
    printf("Failed setting ContainerName - %x\n", hr );
else
    printf( "ContainerName was set to %ws\n", bstrMyName );</pre>
</td>
</tr>
</table></span></div>


