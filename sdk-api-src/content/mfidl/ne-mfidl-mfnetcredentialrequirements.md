---
UID: NE:mfidl._MFNetCredentialRequirements
title: MFNetCredentialRequirements (mfidl.h)
author: windows-sdk-content
description: Specifies how the credential manager should obtain user credentials.
old-location: mf\mfnetcredentialrequirements.htm
tech.root: medfound
ms.assetid: 9257d1d7-7ccb-4172-82f0-3694ebb9d487
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 9257d1d7-7ccb-4172-82f0-3694ebb9d487, MFNetCredentialRequirements, MFNetCredentialRequirements enumeration [Media Foundation], REQUIRE_PROMPT, REQUIRE_SAVE_SELECTED, mf.mfnetcredentialrequirements, mfidl/MFNetCredentialRequirements, mfidl/REQUIRE_PROMPT, mfidl/REQUIRE_SAVE_SELECTED
ms.topic: enum
f1_keywords: 
 - "mfidl/MFNetCredentialRequirements"
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
targetos: Windows
req.typenames: MFNetCredentialRequirements
req.redist: 
ms.custom: 19H1
---

# MFNetCredentialRequirements enumeration


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



The application implements the credential manager, which must expose the <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager">IMFNetCredentialManager</a> interface. If the <b>REQUIRE_PROMPT</b> flag is set, the credential manager should prompt the user for his or her name and password.

The credential cache object sets the <b>REQUIRE_PROMPT</b> flag if the cache does not yet contain valid credentials. It also sets this flag if the credentials will be sent as plain text, unless the credential manager previously set the <b>MFNET_CREDENTIAL_ALLOW_CLEAR_TEXT</b> option. (See <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-setuseroptions">IMFNetCredentialCache::SetUserOptions</a>.)




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfnetcredentialcache-getcredential">IMFNetCredentialCache::GetCredential</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-enumerations">Media Foundation Enumerations</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/network-source-authentication">Network Source Authentication</a>
 

 

