---
UID: NF:wsmandisp.IWSManSession.Enumerate
title: IWSManSession::Enumerate (wsmandisp.h)
description: Enumerates a table, data collection, or log resource.
helpviewer_keywords: ["Enumerate","Enumerate method [Windows Remote Management]","Enumerate method [Windows Remote Management]","IWSManSession interface","IWSManSession interface [Windows Remote Management]","Enumerate method","IWSManSession.Enumerate","IWSManSession::Enumerate","winrm.iwsmansession_enumerate","wsmandisp/IWSManSession::Enumerate"]
old-location: winrm\iwsmansession_enumerate.htm
tech.root: winrm
ms.assetid: b1a4815e-93aa-4a30-a67e-c52fd06c1ee1
ms.date: 12/05/2018
ms.keywords: Enumerate, Enumerate method [Windows Remote Management], Enumerate method [Windows Remote Management],IWSManSession interface, IWSManSession interface [Windows Remote Management],Enumerate method, IWSManSession.Enumerate, IWSManSession::Enumerate, winrm.iwsmansession_enumerate, wsmandisp/IWSManSession::Enumerate
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
req.lib: WSManDisp.tlb
req.dll: WSMAuto.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWSManSession::Enumerate
 - wsmandisp/IWSManSession::Enumerate
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - WSMAuto.dll
api_name:
 - IWSManSession.Enumerate
---

# IWSManSession::Enumerate


## -description

Enumerates a table, data collection, or  log resource. To create a query, include a <i>filter</i> parameter and a <i>dialect</i> parameter in an enumeration.  You can also use an            <a href="/windows/desktop/api/wsmandisp/nn-wsmandisp-iwsmanresourcelocator">IWSManResourceLocator</a> object to create queries. For more information,     see <a href="/windows/desktop/WinRM/enumerating-or-listing-all-instances-of-a-resource">Enumerating or Listing All the Instances of a Resource</a>.

## -parameters

### -param resourceUri [in]

The identifier of the resource to be retrieved.

The following list contains identifiers that this parameter can contain:

<ul>
<li>URI with one or more  <a href="/windows/desktop/WinRM/windows-remote-management-glossary">selectors</a>. When calling the <b>Enumerate</b> method to obtain a WMI resource, use the key property or properties of the object.</li>
<li>You can use <a href="/windows/desktop/WinRM/windows-remote-management-glossary">selectors</a>,  <a href="/windows/desktop/WinRM/windows-remote-management-glossary">fragments</a>, or <a href="/windows/desktop/WinRM/windows-remote-management-glossary">options</a>. For  more information, see <a href="/windows/desktop/api/wsmandisp/nn-wsmandisp-iwsmanresourcelocator">IWSManResourceLocator</a>.</li>
<li><a href="/windows/desktop/WinRM/windows-remote-management-glossary">WS-Addressing</a> endpoint reference as described in the WS-Management protocol  standard.  For more information about the public specification for the WS-Management protocol, see the <a href="/previous-versions/dotnet/articles/ms951267(v=msdn.10)">Management Specifications Index Page</a>.</li>
</ul>

### -param filter [in, optional]

A filter that defines what items in the resource are returned by the enumeration. When the resource is enumerated,  only those items that match the filter criteria are returned. Including a <i>filter</i> parameter and a  <i>dialect</i> parameter in an enumeration converts the enumeration into a query.

If you have an <a href="/windows/desktop/api/wsmandisp/nn-wsmandisp-iwsmanresourcelocator">IWSManResourceLocator</a> object for the <i>resourceURI</i> parameter, then this parameter should not be used. Instead, use the selector and fragment functionality of  <b>IWSManResourceLocator</b>.

### -param dialect [in, optional]

The language used by the filter. <a href="/windows/desktop/WmiSdk/wql-sql-for-wmi">WQL</a>, a subset of SQL used by WMI,  is the only language supported.

If you have a <a href="/windows/desktop/api/wsmandisp/nn-wsmandisp-iwsmanresourcelocator">IWSManResourceLocator</a> object for the <i>resourceURI</i> parameter, then this parameter should not be used. Instead, use the selector and fragment functionality of  <b>IWSManResourceLocator</b>.

### -param flags [in]

This parameter must contain a flag in the <b>__WSManEnumFlags</b> enumeration. For more information, see <a href="/windows/desktop/WinRM/enumeration-constants">Enumeration Constants</a>.

### -param resultSet [out]

An <a href="/windows/desktop/api/wsmandisp/nn-wsmandisp-iwsmanenumerator">IWSManEnumerator</a> object that contains the results of the enumeration.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Call <b>IWSManSession::Enumerate</b> to start an enumeration operation. Thereafter, call <a href="/windows/desktop/api/wsmandisp/nf-wsmandisp-iwsmanenumerator-readitem">IWSManEnumerator::ReadItem</a> using the returned <a href="/windows/desktop/api/wsmandisp/nn-wsmandisp-iwsmanenumerator">IWSManEnumerator</a> object until the end of items is indicated by the <a href="/windows/desktop/api/wsmandisp/nf-wsmandisp-iwsmanenumerator-get_atendofstream">AtEndOfStream</a> property.

Be aware that if the flags include the <a href="/windows/desktop/WinRM/enumeration-constants">Enumeration Constants</a> <b>WSManFlagHierarchyDeepBasePropsOnly</b> or <b>WSManFlagHierarchyShallow</b> then Windows Remote Management service returns the error code <b>ERROR_WSMAN_POLYMORPHISM_MODE_UNSUPPORTED</b>.

For more information about limiting network calls during an enumeration, see the <a href="/windows/desktop/WinRM/session-batchitems">BatchItems</a> property.

If a filter is specified, it must be a valid document with respect to the schema of the resource. The dialect parameter is optional. However, if the filter string begins with &lt;, but is not an XML fragment, then  either  include the <i>dialect</i> parameter or set the <b>WSManFlagNonXmlText</b> flag in the <i>flags</i> parameter. For more information, see <a href="/windows/desktop/WinRM/enumeration-constants">Enumeration Constants</a>.

The corresponding scripting method is <a href="/windows/desktop/WinRM/session-enumerate">Session.Enumerate</a>.

## -see-also

<a href="/windows/desktop/api/wsmandisp/nn-wsmandisp-iwsmanenumerator">IWSManEnumerator</a>



<a href="/windows/desktop/api/wsmandisp/nn-wsmandisp-iwsmansession">IWSManSession</a>



<a href="/windows/desktop/WinRM/session-enumerate">Session.Enumerate</a>