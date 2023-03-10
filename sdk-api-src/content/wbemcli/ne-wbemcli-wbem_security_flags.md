---
UID: NE:wbemcli.tag_WBEM_SECURITY_FLAGS
title: WBEM_SECURITY_FLAGS (wbemcli.h)
description: Contains flags used for setting security access levels.
helpviewer_keywords: ["WBEM_ENABLE","WBEM_FULL_WRITE_REP","WBEM_METHOD_EXECUTE","WBEM_PARTIAL_WRITE_REP","WBEM_REMOTE_ACCESS","WBEM_RIGHT_PUBLISH","WBEM_RIGHT_SUBSCRIBE","WBEM_SECURITY_FLAGS","WBEM_SECURITY_FLAGS enumeration [Windows Management Instrumentation]","WBEM_WRITE_PROVIDER","wbemcli/WBEM_ENABLE","wbemcli/WBEM_FULL_WRITE_REP","wbemcli/WBEM_METHOD_EXECUTE","wbemcli/WBEM_PARTIAL_WRITE_REP","wbemcli/WBEM_REMOTE_ACCESS","wbemcli/WBEM_RIGHT_PUBLISH","wbemcli/WBEM_RIGHT_SUBSCRIBE","wbemcli/WBEM_SECURITY_FLAGS","wbemcli/WBEM_WRITE_PROVIDER","wmi.wbem_security_flags"]
old-location: wmi\wbem_security_flags.htm
tech.root: wmi
ms.assetid: 28415184-B699-42D0-BC5C-0D3E055ABA16
ms.date: 12/05/2018
ms.keywords: WBEM_ENABLE, WBEM_FULL_WRITE_REP, WBEM_METHOD_EXECUTE, WBEM_PARTIAL_WRITE_REP, WBEM_REMOTE_ACCESS, WBEM_RIGHT_PUBLISH, WBEM_RIGHT_SUBSCRIBE, WBEM_SECURITY_FLAGS, WBEM_SECURITY_FLAGS enumeration [Windows Management Instrumentation], WBEM_WRITE_PROVIDER, wbemcli/WBEM_ENABLE, wbemcli/WBEM_FULL_WRITE_REP, wbemcli/WBEM_METHOD_EXECUTE, wbemcli/WBEM_PARTIAL_WRITE_REP, wbemcli/WBEM_REMOTE_ACCESS, wbemcli/WBEM_RIGHT_PUBLISH, wbemcli/WBEM_RIGHT_SUBSCRIBE, wbemcli/WBEM_SECURITY_FLAGS, wbemcli/WBEM_WRITE_PROVIDER, wmi.wbem_security_flags
req.header: wbemcli.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
req.typenames: WBEM_SECURITY_FLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tag_WBEM_SECURITY_FLAGS
 - wbemcli/tag_WBEM_SECURITY_FLAGS
 - WBEM_SECURITY_FLAGS
 - wbemcli/WBEM_SECURITY_FLAGS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wbemcli.h
api_name:
 - WBEM_SECURITY_FLAGS
---

# WBEM_SECURITY_FLAGS enumeration


## -description

Contains flags used for setting security access levels.

## -enum-fields

### -field WBEM_ENABLE:1

Enables the account and grants the user read permissions. This is a default access right for all users and corresponds to the Enable Account permission on the Security tab of the <a href="/windows/desktop/WmiSdk/gloss-w">WMI Control</a>. For more information, see <a href="/windows/desktop/WmiSdk/setting-namespace-security-with-the-wmi-control">Setting Namespace Security with the WMI Control</a>.

### -field WBEM_METHOD_EXECUTE:2

Allows the execution of methods. 


 Providers can perform additional access checks. This is a default access right for all users and corresponds to the Execute Methods permission on the Security tab of the WMI Control.

### -field WBEM_FULL_WRITE_REP:4

Allows a user account to write to classes in the WMI repository as well as instances. A user cannot write to system classes. Only members of the Administrators group have this permission. <b>WBEM_FULL_WRITE_REP</b> corresponds to the Full Write permission on the Security tab of the WMI Control.

### -field WBEM_PARTIAL_WRITE_REP:8

Allows you to write data to instances only, not classes. A user cannot write classes to the <a href="/windows/desktop/WmiSdk/gloss-w">WMI repository</a>. Only members of the Administrators group have this right. <b>WBEM_PARTIAL_WRITE_REP</b> corresponds to the Partial Write permission on the Security tab of the WMI Control.

### -field WBEM_WRITE_PROVIDER:0x10

Allows writing classes and instances to providers. Note that providers can do additional access checks when impersonating a user. This is a default access right for all users and corresponds to the Provider Write permission on the Security tab of the WMI Control.

### -field WBEM_REMOTE_ACCESS:0x20

Allows a user account to remotely perform any operations allowed by the permissions described above. Only members of the Administrators group have this right. <b>WBEM_REMOTE_ACCESS</b> corresponds to the Remote Enable permission on the Security tab of the WMI Control.

### -field WBEM_RIGHT_SUBSCRIBE:0x40

Specifies that a consumer can subscribe to the events delivered to a sink. Used in <a href="/windows/desktop/api/wbemprov/nf-wbemprov-iwbemeventsink-setsinksecurity">IWbemEventSink::SetSinkSecurity</a>.

### -field WBEM_RIGHT_PUBLISH:0x80

Specifies that the account can  publish events to the instance of <a href="/windows/desktop/WmiSdk/--eventfilter">__EventFilter</a> that defines the event filter for a permanent consumer. Available in wbemcli.h.

## -see-also

<a href="/windows/desktop/WmiSdk/event-security-constants">Event Security Constants</a>



<a href="/windows/desktop/WmiSdk/namespace-access-rights-constants">Namespace Access Rights Constants</a>
