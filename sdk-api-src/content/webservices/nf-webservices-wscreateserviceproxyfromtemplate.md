---
UID: NF:webservices.WsCreateServiceProxyFromTemplate
title: WsCreateServiceProxyFromTemplate function (webservices.h)
description: Helper routine for creating a service proxy from policy templates.
helpviewer_keywords: ["WsCreateServiceProxyFromTemplate","WsCreateServiceProxyFromTemplate function [Web Services for Windows]","webservices/WsCreateServiceProxyFromTemplate","wsw.wscreateserviceproxyfromtemplate"]
old-location: wsw\wscreateserviceproxyfromtemplate.htm
tech.root: wsw
ms.assetid: 09a6ee60-ffed-4bab-8747-61c9fee69695
ms.date: 12/05/2018
ms.keywords: WsCreateServiceProxyFromTemplate, WsCreateServiceProxyFromTemplate function [Web Services for Windows], webservices/WsCreateServiceProxyFromTemplate, wsw.wscreateserviceproxyfromtemplate
req.header: webservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: WebServices.lib
req.dll: WebServices.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WsCreateServiceProxyFromTemplate
 - webservices/WsCreateServiceProxyFromTemplate
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - WebServices.dll
api_name:
 - WsCreateServiceProxyFromTemplate
---

# WsCreateServiceProxyFromTemplate function


## -description

Helper routine for creating a <a href="/windows/desktop/wsw/service-proxy">service proxy</a> from policy templates.

## -parameters

### -param channelType [in]

A <a href="/windows/desktop/api/webservices/ne-webservices-ws_channel_type">WS_CHANNEL_TYPE</a> enumeration value representing the channel type for the service proxy.

### -param properties

An array of <a href="/windows/desktop/api/webservices/ns-webservices-ws_proxy_property">WS_PROXY_PROPERTY</a> structures containing optional properties for the service proxy.

The value of this parameter may be <b>NULL</b>, in which case, the <i>propertyCount</i> parameter must be 0 (zero).

### -param propertyCount [in]

The number of properties in the <i>properties</i> array.

### -param templateType [in]

A <a href="/windows/desktop/api/webservices/ne-webservices-ws_binding_template_type">WS_BINDING_TEMPLATE_TYPE</a> enumeration value representing the type of templates  used to create the service proxy.

Please see the <b>Remarks</b> for more information.

### -param templateValue

The optional template structure to be created and filled in by an application. This template structure must be consistent with the input template type (in the <i>templateType</i>). When <i>templateValue</i> parameter is <b>NULL</b>, it is equivalent to the corresponding template structure initialized to zero.

Please see the <b>Remarks</b> for more information.

### -param templateSize [in]

The size, in bytes, of the template structure (in the  <i>templateValue</i> parameter).

### -param templateDescription [in]

The description of <i>templateValue</i>. This must match <i>templateType</i>.

Please see the <b>Remarks</b> for more information.

### -param templateDescriptionSize [in]

The size of the template description.

### -param serviceProxy

On   success, a pointer that receives the address of the  <a href="/windows/desktop/wsw/ws-service-proxy">WS_SERVICE_PROXY</a> structure representing the new service proxy.
                
When you no longer need this structure, you must free it by calling <a href="/windows/desktop/api/webservices/nf-webservices-wsfreeserviceproxy">WsFreeServiceProxy</a>.

### -param error [in, optional]

Pointer to a <a href="/windows/desktop/wsw/ws-error">WS_ERROR</a> structure  that receives additional error information if the function fails.

## -returns

If the function succeeds, it returns NO_ERROR; otherwise, it returns an HRESULT error code.

## -remarks

<b>WsCreateServiceProxyFromTemplate</b> creates the <a href="/windows/desktop/wsw/ws-service-proxy">WS_SERVICE_PROXY</a> structure from input policy templates and additional user input.
      

The following table shows the mapping between <i>templateType</i> values and the corresponding data types to be used in <i>templateValue</i> and <i>templateDescription</i>.

<table>
<tr>
<th>templateType</th>
<th>templateValue</th>
<th>templateDescription</th>
</tr>
<tr>
<td>WS_HTTP_BINDING_TEMPLATE_TYPE</td>
<td>WS_HTTP_BINDING_TEMPLATE</td>
<td>WS_HTTP_POLICY_DESCRIPTION</td>
</tr>
<tr>
<td>WS_HTTP_SSL_BINDING_TEMPLATE_TYPE</td>
<td>WS_HTTP_SSL_BINDING_TEMPLATE</td>
<td>WS_HTTP_SSL_POLICY_DESCRIPTION</td>
</tr>
<tr>
<td>WS_HTTP_HEADER_AUTH_BINDING_TEMPLATE_TYPE</td>
<td>WS_HTTP_HEADER_AUTH_BINDING_TEMPLATE</td>
<td>WS_HTTP_HEADER_AUTH_POLICY_DESCRIPTION</td>
</tr>
<tr>
<td>WS_HTTP_SSL_HEADER_AUTH_BINDING_TEMPLATE_TYPE</td>
<td>WS_HTTP_SSL_HEADER_AUTH_BINDING_TEMPLATE</td>
<td>WS_HTTP_SSL_HEADER_AUTH_POLICY_DESCRIPTION</td>
</tr>
<tr>
<td>WS_HTTP_SSL_USERNAME_BINDING_TEMPLATE_TYPE</td>
<td>WS_HTTP_SSL_USERNAME_BINDING_TEMPLATE</td>
<td>WS_HTTP_SSL_USERNAME_POLICY_DESCRIPTION</td>
</tr>
<tr>
<td>WS_HTTP_SSL_KERBEROS_APREQ_BINDING_TEMPLATE_TYPE</td>
<td>WS_HTTP_SSL_KERBEROS_APREQ_BINDING_TEMPLATE</td>
<td>WS_HTTP_SSL_KERBEROS_APREQ_POLICY_DESCRIPTION</td>
</tr>
<tr>
<td>WS_TCP_BINDING_TEMPLATE_TYPE</td>
<td>WS_TCP_BINDING_TEMPLATE</td>
<td>WS_TCP_POLICY_DESCRIPTION</td>
</tr>
<tr>
<td>WS_TCP_SSPI_BINDING_TEMPLATE_TYPE</td>
<td>WS_TCP_SSPI_BINDING_TEMPLATE</td>
<td>WS_TCP_SSPI_POLICY_DESCRIPTION</td>
</tr>
<tr>
<td>WS_TCP_SSPI_USERNAME_BINDING_TEMPLATE_TYPE</td>
<td>WS_TCP_SSPI_USERNAME_BINDING_TEMPLATE</td>
<td>WS_TCP_SSPI_USERNAME_POLICY_DESCRIPTION</td>
</tr>
<tr>
<td>WS_TCP_SSPI_KERBEROS_APREQ_BINDING_TEMPLATE_TYPE</td>
<td>WS_TCP_SSPI_KERBEROS_APREQ_BINDING_TEMPLATE</td>
<td>WS_TCP_SSPI_KERBEROS_APREQ_POLICY_DESCRIPTION</td>
</tr>
<tr>
<td>WS_HTTP_SSL_USERNAME_SECURITY_CONTEXT_BINDING_TEMPLATE_TYPE</td>
<td>WS_HTTP_SSL_USERNAME_SECURITY_CONTEXT_BINDING_TEMPLATE</td>
<td>WS_HTTP_SSL_USERNAME_SECURITY_CONTEXT_POLICY_DESCRIPTION</td>
</tr>
<tr>
<td>WS_HTTP_SSL_KERBEROS_APREQ_SECURITY_CONTEXT_BINDING_TEMPLATE_TYPE</td>
<td>WS_HTTP_SSL_KERBEROS_APREQ_SECURITY_CONTEXT_BINDING_TEMPLATE</td>
<td>WS_HTTP_SSL_KERBEROS_APREQ_SECURITY_CONTEXT_POLICY_DESCRIPTION</td>
</tr>
<tr>
<td>WS_TCP_SSPI_USERNAME_SECURITY_CONTEXT_BINDING_TEMPLATE_TYPE</td>
<td>WS_TCP_SSPI_USERNAME_SECURITY_CONTEXT_BINDING_TEMPLATE</td>
<td>WS_TCP_SSPI_USERNAME_SECURITY_CONTEXT_POLICY_DESCRIPTION</td>
</tr>
<tr>
<td>WS_TCP_SSPI_KERBEROS_APREQ_SECURITY_CONTEXT_BINDING_TEMPLATE_TYPE</td>
<td>WS_TCP_SSPI_KERBEROS_APREQ_SECURITY_CONTEXT_BINDING_TEMPLATE</td>
<td>WS_TCP_SSPI_KERBEROS_APREQ_SECURITY_CONTEXT_POLICY_DESCRIPTION</td>
</tr>
</table>