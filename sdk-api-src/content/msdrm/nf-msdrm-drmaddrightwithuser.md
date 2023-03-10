---
UID: NF:msdrm.DRMAddRightWithUser
title: DRMAddRightWithUser function (msdrm.h)
description: Assigns a right to a user in an issuance license.
helpviewer_keywords: ["DRMAddRightWithUser","DRMAddRightWithUser function [Active Directory Rights Management Services SDK 1.0]","msdrm/DRMAddRightWithUser","rm.drmaddrightwithuser"]
old-location: rm\drmaddrightwithuser.htm
tech.root: rm
ms.assetid: 10b76b20-cee7-44f3-b9bd-2b690fdd040c
ms.date: 12/05/2018
ms.keywords: DRMAddRightWithUser, DRMAddRightWithUser function [Active Directory Rights Management Services SDK 1.0], msdrm/DRMAddRightWithUser, rm.drmaddrightwithuser
req.header: msdrm.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Msdrm.lib
req.dll: Msdrm.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
req.product: Rights Management Services client 1.0 SP2 or later
ms.custom: 19H1
f1_keywords:
 - DRMAddRightWithUser
 - msdrm/DRMAddRightWithUser
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msdrm.dll
api_name:
 - DRMAddRightWithUser
---

# DRMAddRightWithUser function


## -description

<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="/previous-versions/windows/desktop/msipc/microsoft-information-protection-and-control-client-portal">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRMAddRightWithUser</b> function assigns a right to a user in an issuance license.

## -parameters

### -param hIssuanceLicense [in]

The handle of the issuance license to add the right to. This handle is obtained by using the <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmcreateissuancelicense">DRMCreateIssuanceLicense</a> function.

### -param hRight [in]

The handle of the right to add to the issuance license. This handle is obtained by using the <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmcreateright">DRMCreateRight</a> function.

### -param hUser [in]

The handle of the user to apply the right to. This handle is obtained by using the <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmcreateuser">DRMCreateUser</a> function.

## -returns

If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following list. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

Because there is no way to remove a particular user right   (to remove all user rights, use the <a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmclearallrights">DRMClearAllRights</a> function), we recommend that you collect all user and right information first, and then bind users to rights after all changes have been made.

All rights added must be specifically recognized and handled by the application. An application is not required to handle any standard XrML rights except EDIT. If a user is allowed to edit the content in any way (for example, a user is granted a custom "ADDCOMMENT" right), the user must also be granted the standard XrML EDIT right.

## -see-also

<a href="/previous-versions/windows/desktop/adrms_sdk/ad-rms-functions">AD RMS Functions</a>



<a href="/previous-versions/windows/desktop/adrms_sdk/creating-and-using-issuance-licenses">Creating and Using Issuance Licenses</a>



<a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmcreateissuancelicense">DRMCreateIssuanceLicense</a>



<a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmcreateright">DRMCreateRight</a>



<a href="/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmcreateuser">DRMCreateUser</a>