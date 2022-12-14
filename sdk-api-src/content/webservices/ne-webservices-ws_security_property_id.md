---
UID: NE:webservices.__unnamed_enum_61
title: WS_SECURITY_PROPERTY_ID (webservices.h)
description: Identifies the properties representing channel-wide security settings. This enumeration is used within the WS_SECURITY_PROPERTY structure, which is in turn used within a WS_SECURITY_DESCRIPTION structure.
helpviewer_keywords: ["WS_SECURITY_PROPERTY_ALGORITHM_SUITE","WS_SECURITY_PROPERTY_ALGORITHM_SUITE_NAME","WS_SECURITY_PROPERTY_EXTENDED_PROTECTION_POLICY","WS_SECURITY_PROPERTY_EXTENDED_PROTECTION_SCENARIO","WS_SECURITY_PROPERTY_ID","WS_SECURITY_PROPERTY_ID enumeration [Web Services for Windows]","WS_SECURITY_PROPERTY_MAX_ALLOWED_CLOCK_SKEW","WS_SECURITY_PROPERTY_MAX_ALLOWED_LATENCY","WS_SECURITY_PROPERTY_SECURITY_HEADER_LAYOUT","WS_SECURITY_PROPERTY_SECURITY_HEADER_VERSION","WS_SECURITY_PROPERTY_SERVICE_IDENTITIES","WS_SECURITY_PROPERTY_TIMESTAMP_USAGE","WS_SECURITY_PROPERTY_TIMESTAMP_VALIDITY_DURATION","WS_SECURITY_PROPERTY_TRANSPORT_PROTECTION_LEVEL","webservices/WS_SECURITY_PROPERTY_ALGORITHM_SUITE","webservices/WS_SECURITY_PROPERTY_ALGORITHM_SUITE_NAME","webservices/WS_SECURITY_PROPERTY_EXTENDED_PROTECTION_POLICY","webservices/WS_SECURITY_PROPERTY_EXTENDED_PROTECTION_SCENARIO","webservices/WS_SECURITY_PROPERTY_ID","webservices/WS_SECURITY_PROPERTY_MAX_ALLOWED_CLOCK_SKEW","webservices/WS_SECURITY_PROPERTY_MAX_ALLOWED_LATENCY","webservices/WS_SECURITY_PROPERTY_SECURITY_HEADER_LAYOUT","webservices/WS_SECURITY_PROPERTY_SECURITY_HEADER_VERSION","webservices/WS_SECURITY_PROPERTY_SERVICE_IDENTITIES","webservices/WS_SECURITY_PROPERTY_TIMESTAMP_USAGE","webservices/WS_SECURITY_PROPERTY_TIMESTAMP_VALIDITY_DURATION","webservices/WS_SECURITY_PROPERTY_TRANSPORT_PROTECTION_LEVEL","wsw.ws_security_property_id"]
old-location: wsw\ws_security_property_id.htm
tech.root: wsw
ms.assetid: 98a824c9-11dd-4433-ae8f-2e6b6f6a520f
ms.date: 12/05/2018
ms.keywords: WS_SECURITY_PROPERTY_ALGORITHM_SUITE, WS_SECURITY_PROPERTY_ALGORITHM_SUITE_NAME, WS_SECURITY_PROPERTY_EXTENDED_PROTECTION_POLICY, WS_SECURITY_PROPERTY_EXTENDED_PROTECTION_SCENARIO, WS_SECURITY_PROPERTY_ID, WS_SECURITY_PROPERTY_ID enumeration [Web Services for Windows], WS_SECURITY_PROPERTY_MAX_ALLOWED_CLOCK_SKEW, WS_SECURITY_PROPERTY_MAX_ALLOWED_LATENCY, WS_SECURITY_PROPERTY_SECURITY_HEADER_LAYOUT, WS_SECURITY_PROPERTY_SECURITY_HEADER_VERSION, WS_SECURITY_PROPERTY_SERVICE_IDENTITIES, WS_SECURITY_PROPERTY_TIMESTAMP_USAGE, WS_SECURITY_PROPERTY_TIMESTAMP_VALIDITY_DURATION, WS_SECURITY_PROPERTY_TRANSPORT_PROTECTION_LEVEL, webservices/WS_SECURITY_PROPERTY_ALGORITHM_SUITE, webservices/WS_SECURITY_PROPERTY_ALGORITHM_SUITE_NAME, webservices/WS_SECURITY_PROPERTY_EXTENDED_PROTECTION_POLICY, webservices/WS_SECURITY_PROPERTY_EXTENDED_PROTECTION_SCENARIO, webservices/WS_SECURITY_PROPERTY_ID, webservices/WS_SECURITY_PROPERTY_MAX_ALLOWED_CLOCK_SKEW, webservices/WS_SECURITY_PROPERTY_MAX_ALLOWED_LATENCY, webservices/WS_SECURITY_PROPERTY_SECURITY_HEADER_LAYOUT, webservices/WS_SECURITY_PROPERTY_SECURITY_HEADER_VERSION, webservices/WS_SECURITY_PROPERTY_SERVICE_IDENTITIES, webservices/WS_SECURITY_PROPERTY_TIMESTAMP_USAGE, webservices/WS_SECURITY_PROPERTY_TIMESTAMP_VALIDITY_DURATION, webservices/WS_SECURITY_PROPERTY_TRANSPORT_PROTECTION_LEVEL, wsw.ws_security_property_id
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: WS_SECURITY_PROPERTY_ID
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WS_SECURITY_PROPERTY_ID
 - webservices/WS_SECURITY_PROPERTY_ID
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WebServices.h
api_name:
 - WS_SECURITY_PROPERTY_ID
---

# WS_SECURITY_PROPERTY_ID enumeration


## -description

Identifies the properties representing channel-wide security settings.  This enumeration is used within the <a href="/windows/desktop/api/webservices/ns-webservices-ws_security_property">WS_SECURITY_PROPERTY</a> structure, which is in turn used within a <a href="/windows/desktop/api/webservices/ns-webservices-ws_security_description">WS_SECURITY_DESCRIPTION</a> structure.

## -enum-fields

### -field WS_SECURITY_PROPERTY_TRANSPORT_PROTECTION_LEVEL:1

A <a href="/windows/desktop/api/webservices/ne-webservices-ws_protection_level">WS_PROTECTION_LEVEL</a> value that determines whether signing alone or
          signing plus encryption should be done for the connection.  With at
          least one transport security binding in the security description, the
          default is <b>WS_PROTECTION_LEVEL_SIGN_AND_ENCRYPT</b>.

### -field WS_SECURITY_PROPERTY_ALGORITHM_SUITE:2

With mixed-mode security, this property is a <a href="/windows/win32/api/webservices/ns-webservices-ws_security_algorithm_suite">WS_SECURITY_ALGORITHM_SUITE</a> structure that specifies the algorithm suite to be used. .          
          This property may not be used in conjunction with <a href="/windows/desktop/api/webservices/ne-webservices-ws_security_property_id">WS_SECURITY_PROPERTY_ALGORITHM_SUITE_NAME</a>.
        

If neither this property nor <a href="/windows/win32/api/webservices/ns-webservices-ws_security_algorithm_suite">WS_SECURITY_ALGORITHM_SUITE_NAME</a> is specified, the algorithm
          suite defaults to <b>WS_SECURITY_ALGORITHM_SUITE_NAME_BASIC128</b> when <a href="/windows/desktop/api/webservices/ns-webservices-ws_kerberos_apreq_message_security_binding">WS_KERBEROS_APREQ_MESSAGE_SECURITY_BINDING</a> is used and 
          <b>WS_SECURITY_ALGORITHM_SUITE_NAME_BASIC256</b> otherwise.

### -field WS_SECURITY_PROPERTY_ALGORITHM_SUITE_NAME:3

With mixed-mode security, this property is a  <a href="/windows/desktop/api/webservices/ns-webservices-ws_security_algorithm_suite">WS_SECURITY_ALGORITHM</a> structure that specifies the algorithm suite to be used. The suite names
          refer to collections of algorithms defined 
          in WS-SecurityPolicy 1.1section 7.1.           
          This property may not be used in conjunction with <a href="/windows/desktop/api/webservices/ne-webservices-ws_security_property_id">WS_SECURITY_PROPERTY_ALGORITHM_SUITE</a>.
        

If neither this property nor <a href="/windows/win32/api/webservices/ns-webservices-ws_security_algorithm_suite">WS_SECURITY_ALGORITHM_SUITE</a> is specified, the algorithm
          suite defaults to <a href="/windows/win32/api/webservices/ns-webservices-ws_security_algorithm_suite">WS_SECURITY_ALGORITHM_SUITE_NAME_BASIC128</a> when <a href="/windows/desktop/api/webservices/ns-webservices-ws_kerberos_apreq_message_security_binding">WS_KERBEROS_APREQ_MESSAGE_SECURITY_BINDING</a> is used and 
          <b>WS_SECURITY_ALGORITHM_SUITE_NAME_BASIC256</b> otherwise.

### -field WS_SECURITY_PROPERTY_MAX_ALLOWED_LATENCY:4

With mixed-mode security, this property is a WS_TIMESPAN structure that specifies the maximum allowed staleness of
          an incoming timestamp in the security header. The default is 5 minutes.

### -field WS_SECURITY_PROPERTY_TIMESTAMP_VALIDITY_DURATION:5

With mixed-mode security, this property is a WS_TIMESPAN structure that specifies the timestamp generated by the
          sender will remain valid for this duration from the security
          application instant.  This setting is sometimes called 'time-to-live'
          or 'TTL'. The default is 5 minutes.

### -field WS_SECURITY_PROPERTY_MAX_ALLOWED_CLOCK_SKEW:6

With mixed-mode security, this property is a WS_TIMESPAN structure that specifies the maximum skew allowed between
          the clocks of the sender and receiver.  This quantity serves as a
          margin of tolerance on the enforcement of settings such as <a href="/windows/desktop/api/webservices/ne-webservices-ws_security_property_id">WS_SECURITY_PROPERTY_MAX_ALLOWED_LATENCY</a>.  
          The default is 5 minutes.

### -field WS_SECURITY_PROPERTY_TIMESTAMP_USAGE:7

With mixed-mode security, this property is a <a href="/windows/desktop/api/webservices/ne-webservices-ws_security_timestamp_usage">WS_SECURITY_TIMESTAMP_USAGE</a> value that specifies whether a timestamp should be
          generated (at sender) and demanded (at receiver) in the security
          header.  The default is <b>WS_SECURITY_TIMESTAMP_USAGE_ALWAYS</b>.

### -field WS_SECURITY_PROPERTY_SECURITY_HEADER_LAYOUT:8

With mixed-mode security, this property is a <a href="/windows/desktop/api/webservices/ne-webservices-ws_security_header_layout">WS_SECURITY_HEADER_LAYOUT</a> value that specifies the layout of the security
          header.  The default is <b>WS_SECURITY_HEADER_LAYOUT_STRICT</b>.

### -field WS_SECURITY_PROPERTY_SECURITY_HEADER_VERSION:9

With mixed-mode security, this property is a <a href="/windows/desktop/api/webservices/ne-webservices-ws_security_header_version">WS_SECURITY_HEADER_VERSION</a> value that specifies the WS-Security version to use
          for the security header.  The default is <b>WS_SECURITY_HEADER_VERSION_1_1</b>.

### -field WS_SECURITY_PROPERTY_EXTENDED_PROTECTION_POLICY:10

A <a href="/windows/desktop/api/webservices/ne-webservices-ws_extended_protection_policy">WS_EXTENDED_PROTECTION_POLICY</a> value that specfies whether to validate <a href="/windows/desktop/wsw/extended-protection">Extended Protection</a> data. Only available if extended protection is used.
              

The default is <a href="/windows/desktop/api/webservices/ne-webservices-ws_extended_protection_policy">WS_EXTENDED_PROTECTION_POLICY_WHEN_SUPPORTED</a> on configurations that support extended protection.

This property is only available on the server and can only be used when <a href="/windows/desktop/api/webservices/ne-webservices-ws_channel_binding">WS_HTTP_CHANNEL_BINDING</a> with either <a href="/windows/desktop/api/webservices/ns-webservices-ws_http_header_auth_security_binding">WS_HTTP_HEADER_AUTH_SECURITY_BINDING</a> or <a href="/windows/desktop/api/webservices/ns-webservices-ws_kerberos_apreq_message_security_binding">WS_KERBEROS_APREQ_MESSAGE_SECURITY_BINDING</a> is used.
              

Supported by default on Windows 7 and above. May require an update on systems running earlier versions of Windows. If the operating system was not updated,
                  this property is still available but has no effect.

### -field WS_SECURITY_PROPERTY_EXTENDED_PROTECTION_SCENARIO:11

A <a href="/windows/desktop/api/webservices/ne-webservices-ws_extended_protection_scenario">WS_EXTENDED_PROTECTION_SCENARIO</a> value that specifies the deployment scenario of the server as it pertains to <a href="/windows/desktop/wsw/extended-protection">Extended Protection</a>. Only available if extended protection is used.
              

This property is only available on the server and can only be used when <a href="/windows/desktop/api/webservices/ne-webservices-ws_channel_binding">WS_HTTP_CHANNEL_BINDING</a> with either <a href="/windows/desktop/api/webservices/ns-webservices-ws_http_header_auth_security_binding">WS_HTTP_HEADER_AUTH_SECURITY_BINDING</a> or <a href="/windows/desktop/api/webservices/ns-webservices-ws_kerberos_apreq_message_security_binding">WS_KERBEROS_APREQ_MESSAGE_SECURITY_BINDING</a> is used.
              

The default is <a href="/windows/desktop/api/webservices/ne-webservices-ws_extended_protection_scenario">WS_EXTENDED_PROTECTION_SCENARIO_BOUND_SERVER</a>.

Supported by default on Windows 7 and above. May require an update on systems running earlier versions of Windows. If the operating system was not updated,
                  this property is still available but has no effect.

### -field WS_SECURITY_PROPERTY_SERVICE_IDENTITIES:12

A <a href="/windows/win32/api/webservices/ns-webservices-ws_service_security_identities">WS_SERVICE_SECURITY_IDENTITIES</a> structure that sets the Server Principal Names (SPNs) the server is willing to accept as part of validating <a href="/windows/desktop/wsw/extended-protection">Extended Protection</a> data.
                  SPNs are validated when a <a href="/windows/desktop/api/webservices/ns-webservices-ws_http_header_auth_security_binding">WS_HTTP_HEADER_AUTH_SECURITY_BINDING</a> is used 
                  without a <a href="/windows/desktop/api/webservices/ns-webservices-ws_ssl_transport_security_binding">WS_SSL_TRANSPORT_SECURITY_BINDING</a> or when <a href="/windows/desktop/api/webservices/ne-webservices-ws_extended_protection_scenario">WS_EXTENDED_PROTECTION_SCENARIO_TERMINATED_SSL</a> is set.
              

This property is only available on the server and can only be used with <a href="/windows/desktop/api/webservices/ne-webservices-ws_channel_binding">WS_HTTP_CHANNEL_BINDING</a>.
              

If all of the above requirements are met, this property must be set for security verification to succeed. Otherwise, it must not be set.
              

Supported by default on Windows 7 and above. Requires update to the operating system on other platforms. If the operating system was not updated,
                  this property is still available but has no effect.

## -remarks

All properties defined by the keys here have reasonable defaults; so
        specifying them is optional.  In the common case, one should be able
        to create a <a href="/windows/desktop/api/webservices/ns-webservices-ws_security_description">WS_SECURITY_DESCRIPTION</a> without setting any of
        the properties below.
