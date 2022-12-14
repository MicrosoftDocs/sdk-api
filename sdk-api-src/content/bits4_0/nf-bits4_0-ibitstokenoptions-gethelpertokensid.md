---
UID: NF:bits4_0.IBitsTokenOptions.GetHelperTokenSid
title: IBitsTokenOptions::GetHelperTokenSid (bits4_0.h)
description: Returns the SID of the helper token if one is set.
helpviewer_keywords: ["GetHelperTokenSid","GetHelperTokenSid method [BITS]","GetHelperTokenSid method [BITS]","IBitsTokenOptions interface","IBitsTokenOptions interface [BITS]","GetHelperTokenSid method","IBitsTokenOptions.GetHelperTokenSid","IBitsTokenOptions::GetHelperTokenSid","bits.ibitstokenoptions_gethelpertokensid","bits4_0/IBitsTokenOptions::GetHelperTokenSid"]
old-location: bits\ibitstokenoptions_gethelpertokensid.htm
tech.root: Bits
ms.assetid: 724614af-cae8-47d7-888d-ed1504a9bc12
ms.date: 12/05/2018
ms.keywords: GetHelperTokenSid, GetHelperTokenSid method [BITS], GetHelperTokenSid method [BITS],IBitsTokenOptions interface, IBitsTokenOptions interface [BITS],GetHelperTokenSid method, IBitsTokenOptions.GetHelperTokenSid, IBitsTokenOptions::GetHelperTokenSid, bits.ibitstokenoptions_gethelpertokensid, bits4_0/IBitsTokenOptions::GetHelperTokenSid
req.header: bits4_0.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7
req.target-min-winversvr: Windows Server 2008 R2
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bits4_0.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Windows Management Framework on  Windows Vista with SP1,  Windows Vista with SP2, and  Windows Server 2008 with SP2
ms.custom: 19H1
f1_keywords:
 - IBitsTokenOptions::GetHelperTokenSid
 - bits4_0/IBitsTokenOptions::GetHelperTokenSid
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Bits4_0.h
api_name:
 - IBitsTokenOptions.GetHelperTokenSid
---

# IBitsTokenOptions::GetHelperTokenSid


## -description

Returns the SID of the helper token if one is set.<div class="alert"><b>Note</b>  This method does not return the token.</div>
<div> </div>

## -parameters

### -param pSid [out]

Returns the SID that is retrieved from the <i>TokenInformation</i> parameter of the <a href="/windows/win32/api/securitybaseapi/nf-securitybaseapi-gettokeninformation">GetTokenInformation</a> function.  If no SID is retrieved, this parameter is set to <b>NULL</b>.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Older implementations effectively required that BITS users have  administrator privileges in order to get the helper token SID with this method. Starting with Windows 10, version 1607, non-administrator BITS users can use this method to get the helper token SID on BITS jobs they own. This change enables non-administrator BITS users (such as background downloader services running under the <a href="/windows/desktop/Services/networkservice-account">NetworkService account</a>) to use helper tokens effectively. 

Specifically, the implementation has been changed to allow users without administrator privileges to get the helper token SID, as long as the SID of the  caller's thread's token is the same as the SID of the job owner's user account during the <a href="/windows/desktop/api/bits/nn-bits-ibackgroundcopyjob">IBackgroundCopyJob::QueryInterface</a> call.

## -see-also

<a href="/windows/desktop/api/bits4_0/nn-bits4_0-ibitstokenoptions">IBitsTokenOptions</a>