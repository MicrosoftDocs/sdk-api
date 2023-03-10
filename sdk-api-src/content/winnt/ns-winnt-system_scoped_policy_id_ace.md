---
UID: NS:winnt._SYSTEM_SCOPED_POLICY_ID_ACE
title: SYSTEM_SCOPED_POLICY_ID_ACE (winnt.h)
description: Defines an access control entry (ACE) for the system access control list (SACL) that specifies the scoped policy identifier for a securable object.
helpviewer_keywords: ["*PSYSTEM_SCOPED_POLICY_ID_ACE","PSYSTEM_SCOPED_POLICY_ID_ACE","PSYSTEM_SCOPED_POLICY_ID_ACE structure pointer [Security]","SYSTEM_SCOPED_POLICY_ID_ACE","SYSTEM_SCOPED_POLICY_ID_ACE structure [Security]","_SYSTEM_SCOPED_POLICY_ID_ACE","security.system_scoped_policy_id_ace","winnt/PSYSTEM_SCOPED_POLICY_ID_ACE","winnt/SYSTEM_SCOPED_POLICY_ID_ACE"]
old-location: security\system_scoped_policy_id_ace.htm
tech.root: security
ms.assetid: 6B678A48-E024-4C67-A60C-5224868C04A5
ms.date: 12/05/2018
ms.keywords: '*PSYSTEM_SCOPED_POLICY_ID_ACE, PSYSTEM_SCOPED_POLICY_ID_ACE, PSYSTEM_SCOPED_POLICY_ID_ACE structure pointer [Security], SYSTEM_SCOPED_POLICY_ID_ACE, SYSTEM_SCOPED_POLICY_ID_ACE structure [Security], _SYSTEM_SCOPED_POLICY_ID_ACE, security.system_scoped_policy_id_ace, winnt/PSYSTEM_SCOPED_POLICY_ID_ACE, winnt/SYSTEM_SCOPED_POLICY_ID_ACE'
req.header: winnt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.typenames: SYSTEM_SCOPED_POLICY_ID_ACE, *PSYSTEM_SCOPED_POLICY_ID_ACE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SYSTEM_SCOPED_POLICY_ID_ACE
 - winnt/_SYSTEM_SCOPED_POLICY_ID_ACE
 - PSYSTEM_SCOPED_POLICY_ID_ACE
 - winnt/PSYSTEM_SCOPED_POLICY_ID_ACE
 - SYSTEM_SCOPED_POLICY_ID_ACE
 - winnt/SYSTEM_SCOPED_POLICY_ID_ACE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winnt.h
api_name:
 - SYSTEM_SCOPED_POLICY_ID_ACE
---

# SYSTEM_SCOPED_POLICY_ID_ACE structure


## -description

The <b>SYSTEM_SCOPED_POLICY_ID_ACE</b> structure defines an <a href="/windows/desktop/SecGloss/a-gly">access control entry</a> (ACE) for the <a href="/windows/desktop/SecGloss/s-gly">system access control list</a> (SACL) that specifies the scoped policy identifier for a securable object.

## -struct-fields

### -field Header

An <a href="/windows/desktop/api/winnt/ns-winnt-ace_header">ACE_HEADER</a> structure that specifies the size and type of the ACE. The structure also contains flags that control inheritance of the ACE by child objects. The <b>AceType</b> member of the <b>ACE_HEADER</b> structure must be set to <b>SYSTEM_SCOPED_POLICY_ID_ACE</b>, and the <b>AceSize</b> member must be set to the total number of bytes allocated for the <b>SYSTEM_SCOPED_POLICY_ID_ACE</b> structure.

### -field Mask

The access policy associated with the SACL that contains this ACE.

### -field SidStart

Specifies the first <b>DWORD</b> of a <a href="/windows/desktop/api/winnt/ns-winnt-sid">SID</a>.