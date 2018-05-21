---
UID: NE:webservices.WS_SECURITY_PROPERTY_ID
title: WS_SECURITY_PROPERTY_ID
author: windows-driver-content
description: Identifies the properties representing channel-wide security settings. This enumeration is used within the WS_SECURITY_PROPERTY structure, which is in turn used within a WS_SECURITY_DESCRIPTION structure.
old-location: wsw\ws_security_property_id.htm
old-project: wsw
ms.assetid: 98a824c9-11dd-4433-ae8f-2e6b6f6a520f
ms.author: windowsdriverdev
ms.date: 5/18/2018
ms.keywords: WS_SECURITY_PROPERTY_ALGORITHM_SUITE, WS_SECURITY_PROPERTY_ALGORITHM_SUITE_NAME, WS_SECURITY_PROPERTY_EXTENDED_PROTECTION_POLICY, WS_SECURITY_PROPERTY_EXTENDED_PROTECTION_SCENARIO, WS_SECURITY_PROPERTY_ID, WS_SECURITY_PROPERTY_ID enumeration [Web Services for Windows], WS_SECURITY_PROPERTY_MAX_ALLOWED_CLOCK_SKEW, WS_SECURITY_PROPERTY_MAX_ALLOWED_LATENCY, WS_SECURITY_PROPERTY_SECURITY_HEADER_LAYOUT, WS_SECURITY_PROPERTY_SECURITY_HEADER_VERSION, WS_SECURITY_PROPERTY_SERVICE_IDENTITIES, WS_SECURITY_PROPERTY_TIMESTAMP_USAGE, WS_SECURITY_PROPERTY_TIMESTAMP_VALIDITY_DURATION, WS_SECURITY_PROPERTY_TRANSPORT_PROTECTION_LEVEL, webservices/WS_SECURITY_PROPERTY_ALGORITHM_SUITE, webservices/WS_SECURITY_PROPERTY_ALGORITHM_SUITE_NAME, webservices/WS_SECURITY_PROPERTY_EXTENDED_PROTECTION_POLICY, webservices/WS_SECURITY_PROPERTY_EXTENDED_PROTECTION_SCENARIO, webservices/WS_SECURITY_PROPERTY_ID, webservices/WS_SECURITY_PROPERTY_MAX_ALLOWED_CLOCK_SKEW, webservices/WS_SECURITY_PROPERTY_MAX_ALLOWED_LATENCY, webservices/WS_SECURITY_PROPERTY_SECURITY_HEADER_LAYOUT, webservices/WS_SECURITY_PROPERTY_SECURITY_HEADER_VERSION, webservices/WS_SECURITY_PROPERTY_SERVICE_IDENTITIES, webservices/WS_SECURITY_PROPERTY_TIMESTAMP_USAGE, webservices/WS_SECURITY_PROPERTY_TIMESTAMP_VALIDITY_DURATION, webservices/WS_SECURITY_PROPERTY_TRANSPORT_PROTECTION_LEVEL, wsw.ws_security_property_id
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: webservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WS_SECURITY_PROPERTY_ID
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	WebServices.h
api_name:
-	WS_SECURITY_PROPERTY_ID
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# WS_SECURITY_PROPERTY_ID enumeration


## -description



        Identifies the properties representing channel-wide security settings.  This enumeration is used within the <a href="https://msdn.microsoft.com/676079cd-6ca8-486b-9604-172423210ad5">WS_SECURITY_PROPERTY</a> structure, which is in turn used within a <a href="https://msdn.microsoft.com/b9490f00-877c-4d9f-b361-eaca343cdee0">WS_SECURITY_DESCRIPTION</a> structure.
      


## -enum-fields




### -field WS_SECURITY_PROPERTY_TRANSPORT_PROTECTION_LEVEL


          A <a href="https://msdn.microsoft.com/2b673728-1050-4005-bbb6-64b81ec19174">WS_PROTECTION_LEVEL</a> value that determines whether signing alone or
          signing plus encryption should be done for the connection.  With at
          least one transport security binding in the security description, the
          default is <b>WS_PROTECTION_LEVEL_SIGN_AND_ENCRYPT</b>.
        


### -field WS_SECURITY_PROPERTY_ALGORITHM_SUITE


          With mixed-mode security, this property is a <a href="https://msdn.microsoft.com/aa2bb951-47ba-4241-b29a-2f54b92da4cb">WS_SECURITY_ALGORITHM_SUITE</a> structure that specifies the algorithm suite to be used. .          
          This property may not be used in conjunction with <a href="https://msdn.microsoft.com/98a824c9-11dd-4433-ae8f-2e6b6f6a520f">WS_SECURITY_PROPERTY_ALGORITHM_SUITE_NAME</a>.
        


          If neither this property nor <a href="https://msdn.microsoft.com/cd7116d2-86f6-475e-a55d-050c7e02172d">WS_SECURITY_ALGORITHM_SUITE_NAME</a> is specified, the algorithm
          suite defaults to <b>WS_SECURITY_ALGORITHM_SUITE_NAME_BASIC128</b>
 
          when <a href="https://msdn.microsoft.com/03127248-f5cc-44da-9c3d-abf016dd6bb2">WS_KERBEROS_APREQ_MESSAGE_SECURITY_BINDING</a> is used and 
          <b>WS_SECURITY_ALGORITHM_SUITE_NAME_BASIC256</b> otherwise.
        


### -field WS_SECURITY_PROPERTY_ALGORITHM_SUITE_NAME

With mixed-mode security, this property is a  <a href="https://msdn.microsoft.com/aa2bb951-47ba-4241-b29a-2f54b92da4cb">WS_SECURITY_ALGORITHM</a> structure that specifies the algorithm suite to be used. The suite names
          refer to collections of algorithms defined 
          in WS-SecurityPolicy 1.1
          section 7.1.           
          This property may not be used in conjunction with <a href="https://msdn.microsoft.com/98a824c9-11dd-4433-ae8f-2e6b6f6a520f">WS_SECURITY_PROPERTY_ALGORITHM_SUITE</a>.
        


          If neither this property nor <a href="https://msdn.microsoft.com/aa2bb951-47ba-4241-b29a-2f54b92da4cb">WS_SECURITY_ALGORITHM_SUITE</a> is specified, the algorithm
          suite defaults to <a href="https://msdn.microsoft.com/cd7116d2-86f6-475e-a55d-050c7e02172d">WS_SECURITY_ALGORITHM_SUITE_NAME_BASIC128</a>

          when <a href="https://msdn.microsoft.com/03127248-f5cc-44da-9c3d-abf016dd6bb2">WS_KERBEROS_APREQ_MESSAGE_SECURITY_BINDING</a> is used and 
          <b>WS_SECURITY_ALGORITHM_SUITE_NAME_BASIC256</b> otherwise.
        


### -field WS_SECURITY_PROPERTY_MAX_ALLOWED_LATENCY

With mixed-mode security, this property is a WS_TIMESPAN structure that specifies the maximum allowed staleness of
          an incoming timestamp in the security header. The default is 5 minutes.
        


### -field WS_SECURITY_PROPERTY_TIMESTAMP_VALIDITY_DURATION


          With mixed-mode security, this property is a WS_TIMESPAN structure that specifies the timestamp generated by the
          sender will remain valid for this duration from the security
          application instant.  This setting is sometimes called 'time-to-live'
          or 'TTL'. The default is 5 minutes.
        


### -field WS_SECURITY_PROPERTY_MAX_ALLOWED_CLOCK_SKEW


          With mixed-mode security, this property is a WS_TIMESPAN structure that specifies the maximum skew allowed between
          the clocks of the sender and receiver.  This quantity serves as a
          margin of tolerance on the enforcement of settings such as <a href="https://msdn.microsoft.com/98a824c9-11dd-4433-ae8f-2e6b6f6a520f">WS_SECURITY_PROPERTY_MAX_ALLOWED_LATENCY</a>.  
          The default is 5 minutes.
        


### -field WS_SECURITY_PROPERTY_TIMESTAMP_USAGE

With mixed-mode security, this property is a <a href="https://msdn.microsoft.com/72e2a404-7988-40b8-b9ec-f9b9b3d767c1">WS_SECURITY_TIMESTAMP_USAGE</a> value that specifies whether a timestamp should be
          generated (at sender) and demanded (at receiver) in the security
          header.  The default is <b>WS_SECURITY_TIMESTAMP_USAGE_ALWAYS</b>.
        


### -field WS_SECURITY_PROPERTY_SECURITY_HEADER_LAYOUT

With mixed-mode security, this property is a <a href="https://msdn.microsoft.com/a3090e6f-1f80-4d67-b7d7-1165486dcc66">WS_SECURITY_HEADER_LAYOUT</a> value that specifies the layout of the security
          header.  The default is <b>WS_SECURITY_HEADER_LAYOUT_STRICT</b>.
        


### -field WS_SECURITY_PROPERTY_SECURITY_HEADER_VERSION


          With mixed-mode security, this property is a <a href="https://msdn.microsoft.com/27093dc0-f4aa-4602-a51c-76633358792a">WS_SECURITY_HEADER_VERSION</a> value that specifies the WS-Security version to use
          for the security header.  The default is <b>WS_SECURITY_HEADER_VERSION_1_1</b>.
        


### -field WS_SECURITY_PROPERTY_EXTENDED_PROTECTION_POLICY


                  A <a href="https://msdn.microsoft.com/ee3685b1-0ffe-410e-a6fc-b31ed8d25b26">WS_EXTENDED_PROTECTION_POLICY</a> value that specfies whether to validate <a href="https://msdn.microsoft.com/35e48846-05e5-4db9-a3b5-098b62815b66">Extended Protection</a> data. Only available if extended protection is used.
              

The default is <a href="https://msdn.microsoft.com/ee3685b1-0ffe-410e-a6fc-b31ed8d25b26">WS_EXTENDED_PROTECTION_POLICY_WHEN_SUPPORTED</a> on configurations that support extended protection.


                  This property is only available on the server and can only be used when <a href="https://msdn.microsoft.com/554cc239-feab-4262-9821-6478a3d93ffc">WS_HTTP_CHANNEL_BINDING</a> with either <a href="https://msdn.microsoft.com/c6ca6760-a927-470f-9785-7500d1711902">WS_HTTP_HEADER_AUTH_SECURITY_BINDING</a>
                  or <a href="https://msdn.microsoft.com/03127248-f5cc-44da-9c3d-abf016dd6bb2">WS_KERBEROS_APREQ_MESSAGE_SECURITY_BINDING</a> is used.
              


                  Supported by default on Windows 7 and above. May require an update on systems running earlier versions of Windows. If the operating system was not updated,
                  this property is still available but has no effect.
              


### -field WS_SECURITY_PROPERTY_EXTENDED_PROTECTION_SCENARIO


                  A <a href="https://msdn.microsoft.com/bd4a41aa-10bc-445c-9664-49f284881bf8">WS_EXTENDED_PROTECTION_SCENARIO</a> value that specifes the deployment scenario of the server as it pertains to <a href="https://msdn.microsoft.com/35e48846-05e5-4db9-a3b5-098b62815b66">Extended Protection</a>. Only available if extended protection is used.
              


                  This property is only available on the server and can only be used when <a href="https://msdn.microsoft.com/554cc239-feab-4262-9821-6478a3d93ffc">WS_HTTP_CHANNEL_BINDING</a> with either <a href="https://msdn.microsoft.com/c6ca6760-a927-470f-9785-7500d1711902">WS_HTTP_HEADER_AUTH_SECURITY_BINDING</a>
                  or <a href="https://msdn.microsoft.com/03127248-f5cc-44da-9c3d-abf016dd6bb2">WS_KERBEROS_APREQ_MESSAGE_SECURITY_BINDING</a> is used.
              

The default is <a href="https://msdn.microsoft.com/bd4a41aa-10bc-445c-9664-49f284881bf8">WS_EXTENDED_PROTECTION_SCENARIO_BOUND_SERVER</a>.


                  Supported by default on Windows 7 and above. May require an update on systems running earlier versions of Windows. If the operating system was not updated,
                  this property is still available but has no effect.
              


### -field WS_SECURITY_PROPERTY_SERVICE_IDENTITIES

A <a href="https://msdn.microsoft.com/d38f0efd-2570-4db1-b4f7-113a45fe4449">WS_SERVICE_SECURITY_IDENTITIES</a> structure that sets the Server Principal Names (SPNs) the server is willing to accept as part of validating <a href="https://msdn.microsoft.com/35e48846-05e5-4db9-a3b5-098b62815b66">Extended Protection</a> data.
                  SPNs are validated when a <a href="https://msdn.microsoft.com/c6ca6760-a927-470f-9785-7500d1711902">WS_HTTP_HEADER_AUTH_SECURITY_BINDING</a> is used 
                  without a <a href="https://msdn.microsoft.com/078efc1d-a1bc-4035-919c-f927a8ceb8e6">WS_SSL_TRANSPORT_SECURITY_BINDING</a> or when <a href="https://msdn.microsoft.com/bd4a41aa-10bc-445c-9664-49f284881bf8">WS_EXTENDED_PROTECTION_SCENARIO_TERMINATED_SSL</a> is set.
              


                  This property is only available on the server and can only be used with <a href="https://msdn.microsoft.com/554cc239-feab-4262-9821-6478a3d93ffc">WS_HTTP_CHANNEL_BINDING</a>.
              


                  If all of the above requirements are met, this property must be set for security verification to succeed. Otherwise, it must not be set.
              


                  Supported by default on Windows 7 and above. Requires update to the operating system on other platforms. If the operating system was not updated,
                  this property is still available but has no effect.
              


## -remarks




        All properties defined by the keys here have reasonable defaults; so
        specifying them is optional.  In the common case, one should be able
        to create a <a href="https://msdn.microsoft.com/b9490f00-877c-4d9f-b361-eaca343cdee0">WS_SECURITY_DESCRIPTION</a> without setting any of
        the properties below.
      



