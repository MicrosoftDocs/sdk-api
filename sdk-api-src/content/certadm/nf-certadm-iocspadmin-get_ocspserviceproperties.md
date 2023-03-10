---
UID: NF:certadm.IOCSPAdmin.get_OCSPServiceProperties
title: IOCSPAdmin::get_OCSPServiceProperties (certadm.h)
description: Gets an instance of an OCSPPropertyCollection object. This object represents the attributes of an Online Certificate Status Protocol (OCSP) responder service.
old-location: security\iocspadmin_ocspserviceproperties_method.htm
tech.root: security
ms.assetid: d792283b-dde9-46b7-8483-b3011b4433eb
ms.date: 12/05/2018
ms.keywords: IOCSPAdmin interface [Security],OCSPServiceProperties property, IOCSPAdmin.OCSPServiceProperties, IOCSPAdmin.get_OCSPServiceProperties, IOCSPAdmin::OCSPServiceProperties, IOCSPAdmin::get_OCSPServiceProperties, OCSPServiceProperties property [Security], OCSPServiceProperties property [Security],IOCSPAdmin interface, certadm/IOCSPAdmin::OCSPServiceProperties, certadm/IOCSPAdmin::get_OCSPServiceProperties, get_OCSPServiceProperties, security.iocspadmin_ocspserviceproperties_method
req.header: certadm.h
req.include-header: Certsrv.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 Datacenter, Windows Server 2008 Enterprise [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Certadm.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Certadm.lib
req.dll: Certadm.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IOCSPAdmin::get_OCSPServiceProperties
 - certadm/IOCSPAdmin::get_OCSPServiceProperties
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certadm.dll
api_name:
 - IOCSPAdmin.OCSPServiceProperties
 - IOCSPAdmin.get_OCSPServiceProperties
---

# IOCSPAdmin::get_OCSPServiceProperties


## -description

The <b>OCSPServiceProperties</b> property gets  an instance of an <a href="/windows/desktop/api/certadm/nn-certadm-iocsppropertycollection">OCSPPropertyCollection</a> object. This object represents the attributes of an Online Certificate Status Protocol (OCSP) responder service. After instantiating an <a href="/windows/desktop/api/certadm/nn-certadm-iocspadmin">OCSPAdmin</a> object, a script or administration tool can use the retrieved <a href="/windows/desktop/api/certadm/nn-certadm-iocsppropertycollection">IOCSPPropertyCollection</a> interface  to expose responder-service attributes.

This property is read-only.

## -parameters

## -remarks

The following table lists the possible <a href="/windows/desktop/api/certadm/nf-certadm-iocspproperty-get_name">Name</a>-<a href="/windows/desktop/api/certadm/nf-certadm-iocspproperty-get_value">Value</a> pairs for OCSP service properties.

<table>
<tr>
<th>Name</th>
<th>Value</th>
</tr>
<tr>
<td><b>LogLevel</b></td>
<td>
The <a href="/windows/desktop/api/certadm/nf-certadm-iocspproperty-get_value">Value</a> of <b>LogLevel</b> must be one of the following constants.



<dl>
<dt><a id="Constant__CERTLOG_MINIMAL"></a><a id="constant__certlog_minimal"></a><a id="CONSTANT__CERTLOG_MINIMAL"></a>Constant: CERTLOG_MINIMAL</dt>
<dd>
<b>DWORD</b>: 0

</dd>
<dt><a id="Constant__CERTLOG_TERSE"></a><a id="constant__certlog_terse"></a><a id="CONSTANT__CERTLOG_TERSE"></a>Constant: CERTLOG_TERSE</dt>
<dd>
<b>DWORD</b>: 1

</dd>
<dt><a id="Constant__CERTLOG_ERROR"></a><a id="constant__certlog_error"></a><a id="CONSTANT__CERTLOG_ERROR"></a>Constant: CERTLOG_ERROR</dt>
<dd>
<b>DWORD</b>: 2

</dd>
<dt><a id="Constant__CERTLOG_WARNING"></a><a id="constant__certlog_warning"></a><a id="CONSTANT__CERTLOG_WARNING"></a>Constant: CERTLOG_WARNING</dt>
<dd>
<b>DWORD</b>: 3 (default)

</dd>
<dt><a id="Constant__CERTLOG_VERBOSE"></a><a id="constant__certlog_verbose"></a><a id="CONSTANT__CERTLOG_VERBOSE"></a>Constant: CERTLOG_VERBOSE</dt>
<dd>
<b>DWORD</b>: 4

</dd>
<dt><a id="Constant__CERTLOG_EXHAUSTIVE"></a><a id="constant__certlog_exhaustive"></a><a id="CONSTANT__CERTLOG_EXHAUSTIVE"></a>Constant: CERTLOG_EXHAUSTIVE</dt>
<dd>
<b>DWORD</b>: 5

</dd>
</dl>
</td>
</tr>
<tr>
<td><b>AuditFilter</b></td>
<td>
The <a href="/windows/desktop/api/certadm/nf-certadm-iocspproperty-get_value">Value</a> of <b>AuditFilter</b> can be any bitwise combination of the following <b>DWORD</b> values.



<dl>
<dt><a id="Description__Audit_OCSP_service_start_stop"></a><a id="description__audit_ocsp_service_start_stop"></a><a id="DESCRIPTION__AUDIT_OCSP_SERVICE_START_STOP"></a>Description: Audit OCSP service start/stop</dt>
<dd>
<b>DWORD</b>: 0x1

</dd>
<dt><a id="Description__Changes_to_the_OCSP_configuration"></a><a id="description__changes_to_the_ocsp_configuration"></a><a id="DESCRIPTION__CHANGES_TO_THE_OCSP_CONFIGURATION"></a>Description: Changes to the OCSP configuration</dt>
<dd>
<b>DWORD</b>: 0x2

</dd>
<dt><a id="Description__Requests_submitted_to_the_OCSP"></a><a id="description__requests_submitted_to_the_ocsp"></a><a id="DESCRIPTION__REQUESTS_SUBMITTED_TO_THE_OCSP"></a>Description: Requests submitted to the OCSP</dt>
<dd>
<b>DWORD</b>: 0x4

</dd>
<dt><a id="Description__Changes_to_the_OCSP_security_settings"></a><a id="description__changes_to_the_ocsp_security_settings"></a><a id="DESCRIPTION__CHANGES_TO_THE_OCSP_SECURITY_SETTINGS"></a>Description: Changes to the OCSP security settings</dt>
<dd>
<b>DWORD</b>: 0x8

</dd>
</dl>
</td>
</tr>
<tr>
<td><b>ArrayController</b></td>
<td>
The <a href="/windows/desktop/api/certadm/nf-certadm-iocspproperty-get_value">Value</a> of <b>ArrayController</b> must be a string that represents the computer name of the OCSP server that acts as the array controller for an OCSP array configuration.

</td>
</tr>
<tr>
<td><b>ArrayMembers</b></td>
<td>
The <a href="/windows/desktop/api/certadm/nf-certadm-iocspproperty-get_value">Value</a> of <b>ArrayMembers</b> can be a multiple-line string that represents the computer names of the OCSP servers that are part of an OCSP array configuration.

</td>
</tr>
<tr>
<td><b>EnrollPollInterval</b></td>
<td>
The <a href="/windows/desktop/api/certadm/nf-certadm-iocspproperty-get_value">Value</a> of <b>EnrollPollInterval</b> must be a <b>DWORD</b> value from 0 to 24 that represents the number of hours between OCSP service certificate enrollment attempts. This interval determines how often the service checks the status of target certificates for a template change or pending validity change. When the service finds a change, it attempts to enroll for a new certificate.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/certadm/nn-certadm-iocspadmin">IOCSPAdmin</a>