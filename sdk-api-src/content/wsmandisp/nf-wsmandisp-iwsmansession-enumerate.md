---
UID: NF:wsmandisp.IWSManSession.Enumerate
title: IWSManSession::Enumerate
author: windows-sdk-content
description: Enumerates a table, data collection, or log resource.
old-location: winrm\iwsmansession_enumerate.htm
old-project: WinRM
ms.assetid: b1a4815e-93aa-4a30-a67e-c52fd06c1ee1
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: Enumerate, Enumerate method [Windows Remote Management], Enumerate method [Windows Remote Management],IWSManSession interface, IWSManSession interface [Windows Remote Management],Enumerate method, IWSManSession.Enumerate, IWSManSession::Enumerate, winrm.iwsmansession_enumerate, wsmandisp/IWSManSession::Enumerate
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wsmandisp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WSManDisp.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WSManProxyAuthenticationFlags
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - WSMAuto.dll
api_name:
 - IWSManSession.Enumerate
product: Windows
targetos: Windows
req.lib: WSManDisp.tlb
req.dll: WSMAuto.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWSManSession::Enumerate


## -description


Enumerates a table, data collection, or  log resource. To create a query, include a <i>filter</i> parameter and a <i>dialect</i> parameter in an enumeration.  You can also use an            <a href="https://msdn.microsoft.com/7b3dcb53-d02c-4ba6-973d-1493ba442387">IWSManResourceLocator</a> object to create queries. For more information,     see <a href="https://msdn.microsoft.com/c50c37bf-e19a-473b-8d27-ab3bb4ec86a0">Enumerating or Listing All the Instances of a Resource</a>.


## -parameters




### -param resourceUri [in]

The identifier of the resource to be retrieved.

The following list contains identifiers that this parameter can contain:

<ul>
<li>URI with one or more  <a href="https://msdn.microsoft.com/en-us/library/Aa384465(v=VS.85).aspx">selectors</a>. When calling the <b>Enumerate</b> method to obtain a WMI resource, use the key property or properties of the object.</li>
<li>You can use <a href="https://msdn.microsoft.com/en-us/library/Aa384465(v=VS.85).aspx">selectors</a>,  <a href="https://msdn.microsoft.com/en-us/library/Aa384465(v=VS.85).aspx">fragments</a>, or <a href="https://msdn.microsoft.com/library/windows/hardware/dn965779">options</a>. For  more information, see <a href="https://msdn.microsoft.com/7b3dcb53-d02c-4ba6-973d-1493ba442387">IWSManResourceLocator</a>.</li>
<li><a href="https://msdn.microsoft.com/en-us/library/Aa384465(v=VS.85).aspx">WS-Addressing</a> endpoint reference as described in the WS-Management protocol  standard.  For more information about the public specification for the WS-Management protocol, see the <a href="http://go.microsoft.com/fwlink/p/?linkid=84316">Management Specifications Index Page</a>.</li>
</ul>

### -param filter [in, optional]

A filter that defines what items in the resource are returned by the enumeration. When the resource is enumerated,  only those items that match the filter criteria are returned. Including a <i>filter</i> parameter and a  <i>dialect</i> parameter in an enumeration converts the enumeration into a query.

If you have an <a href="https://msdn.microsoft.com/7b3dcb53-d02c-4ba6-973d-1493ba442387">IWSManResourceLocator</a> object for the <i>resourceURI</i> parameter, then this parameter should not be used. Instead, use the selector and fragment functionality of  <b>IWSManResourceLocator</b>.


### -param dialect [in, optional]

The language used by the filter. <a href="https://msdn.microsoft.com/72a7ec04-9af3-41ae-9189-6e1d46803fa9">WQL</a>, a subset of SQL used by WMI,  is the only language supported.

If you have a <a href="https://msdn.microsoft.com/7b3dcb53-d02c-4ba6-973d-1493ba442387">IWSManResourceLocator</a> object for the <i>resourceURI</i> parameter, then this parameter should not be used. Instead, use the selector and fragment functionality of  <b>IWSManResourceLocator</b>.


### -param flags [in]

This parameter must contain a flag in the <b>__WSManEnumFlags</b> enumeration. For more information, see <a href="https://msdn.microsoft.com/c0f2763b-a549-43d5-84a6-8cebf33a1ea2">Enumeration Constants</a>.


### -param resultSet [out]

An <a href="https://msdn.microsoft.com/c7afac5d-946f-49ec-a7d0-de558ed2144b">IWSManEnumerator</a> object that contains the results of the enumeration.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Call <b>IWSManSession::Enumerate</b> to start an enumeration operation. Thereafter, call <a href="https://msdn.microsoft.com/6b181a4b-347c-4874-969c-9ca7d36ec788">IWSManEnumerator::ReadItem</a> using the returned <a href="https://msdn.microsoft.com/c7afac5d-946f-49ec-a7d0-de558ed2144b">IWSManEnumerator</a> object until the end of items is indicated by the <a href="https://msdn.microsoft.com/d80028b0-04ff-4c6d-90f5-1c81141a956c">AtEndOfStream</a> property.

Be aware that if the flags include the <a href="https://msdn.microsoft.com/c0f2763b-a549-43d5-84a6-8cebf33a1ea2">Enumeration Constants</a> <b>WSManFlagHierarchyDeepBasePropsOnly</b> or <b>WSManFlagHierarchyShallow</b> then Windows Remote Management service returns the error code <b>ERROR_WSMAN_POLYMORPHISM_MODE_UNSUPPORTED</b>.

For more information about limiting network calls during an enumeration, see the <a href="https://msdn.microsoft.com/1675ba12-a0c7-4e59-a013-2109780e8afe">BatchItems</a> property.

If a filter is specified, it must be a valid document with respect to the schema of the resource. The dialect parameter is optional. However, if the filter string begins with &lt;, but is not an XML fragment, then  either  include the <i>dialect</i> parameter or set the <b>WSManFlagNonXmlText</b> flag in the <i>flags</i> parameter. For more information, see <a href="https://msdn.microsoft.com/c0f2763b-a549-43d5-84a6-8cebf33a1ea2">Enumeration Constants</a>.

The corresponding scripting method is <a href="https://msdn.microsoft.com/ed8ad3ad-d033-45cb-b681-995c5f73b12e">Session.Enumerate</a>.




## -see-also




<a href="https://msdn.microsoft.com/c7afac5d-946f-49ec-a7d0-de558ed2144b">IWSManEnumerator</a>



<a href="https://msdn.microsoft.com/3e016080-339f-4bda-bfd2-f912e090981f">IWSManSession</a>



<a href="https://msdn.microsoft.com/ed8ad3ad-d033-45cb-b681-995c5f73b12e">Session.Enumerate</a>
 

 

