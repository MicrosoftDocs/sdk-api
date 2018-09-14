---
UID: NE:mfidl._MFNetCredentialRequirements
title: "_MFNetCredentialRequirements"
author: windows-sdk-content
description: Specifies how the credential manager should obtain user credentials.
old-location: mf\mfnetcredentialrequirements.htm
tech.root: medfound
ms.assetid: 9257d1d7-7ccb-4172-82f0-3694ebb9d487
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: 9257d1d7-7ccb-4172-82f0-3694ebb9d487, MFNetCredentialRequirements, MFNetCredentialRequirements enumeration [Media Foundation], REQUIRE_PROMPT, REQUIRE_SAVE_SELECTED, _MFNetCredentialRequirements, mf.mfnetcredentialrequirements, mfidl/MFNetCredentialRequirements, mfidl/REQUIRE_PROMPT, mfidl/REQUIRE_SAVE_SELECTED
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mfidl.h
api_name:
 - MFNetCredentialRequirements
product: Windows
targetos: Windows
req.typenames: MFNetCredentialRequirements
req.redist: 
---

# _MFNetCredentialRequirements enumeration


## -description


Specifies how the credential manager should obtain user credentials.
        


## -enum-fields




### -field REQUIRE_PROMPT

The credential manager should prompt the user to provide the credentials.
          


### -field REQUIRE_SAVE_SELECTED


<div class="alert"><b>Note</b>  Requires Windows 7 or later.</div>
<div> </div>


The credentials are saved to persistent storage. This flag acts as a hint for the application's UI. If the application prompts the user for credentials, the UI can indicate that the credentials have already been saved.


## -remarks



The application implements the credential manager, which must expose the <a href="https://msdn.microsoft.com/002d8608-4ef9-40fd-8dcc-fe6ade34478e">IMFNetCredentialManager</a> interface. If the <b>REQUIRE_PROMPT</b> flag is set, the credential manager should prompt the user for his or her name and password.

The credential cache object sets the <b>REQUIRE_PROMPT</b> flag if the cache does not yet contain valid credentials. It also sets this flag if the credentials will be sent as plain text, unless the credential manager previously set the <b>MFNET_CREDENTIAL_ALLOW_CLEAR_TEXT</b> option. (See <a href="https://msdn.microsoft.com/024eea57-e7c8-495d-9959-ab37dd45873d">IMFNetCredentialCache::SetUserOptions</a>.)




## -see-also




<a href="https://msdn.microsoft.com/7e095445-354a-4fbb-b354-bf87eb77552f">IMFNetCredentialCache::GetCredential</a>



<a href="https://msdn.microsoft.com/f26a730f-18c4-4247-acaf-af1dfad19086">Media Foundation Enumerations</a>



<a href="https://msdn.microsoft.com/bffc33ec-0fb0-4bbe-9bac-583b9d4e1153">Network Source Authentication</a>
 

 

