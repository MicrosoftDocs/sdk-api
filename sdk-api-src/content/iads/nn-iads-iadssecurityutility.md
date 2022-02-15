---
UID: NN:iads.IADsSecurityUtility
title: IADsSecurityUtility (iads.h)
description: The IADsSecurityUtility interface is used to get, set, or retrieve the security descriptor on a file, fileshare, or registry key.
helpviewer_keywords: ["IADsSecurityUtility","IADsSecurityUtility interface [ADSI]","IADsSecurityUtility interface [ADSI]","described","_ds_iadssecurityutility","adsi.iadssecurityutility","iads/IADsSecurityUtility"]
old-location: adsi\iadssecurityutility.htm
tech.root: adsi
ms.assetid: 781eda1e-1f13-4bb4-ae8e-c9bf4c08e125
ms.date: 12/05/2018
ms.keywords: IADsSecurityUtility, IADsSecurityUtility interface [ADSI], IADsSecurityUtility interface [ADSI],described, _ds_iadssecurityutility, adsi.iadssecurityutility, iads/IADsSecurityUtility
req.header: iads.h
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
req.dll: Activeds.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IADsSecurityUtility
 - iads/IADsSecurityUtility
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Activeds.dll
api_name:
 - IADsSecurityUtility
---

# IADsSecurityUtility interface


## -description

The <b>IADsSecurityUtility</b> interface is used to get, set, or retrieve the security descriptor on a file, fileshare, or registry key. You can also use it to convert the security descriptor to or from raw or hexadecimal mode and you can limit the scope of the security descriptor data retrieved or set by indicating whether you want it for the owner, group, DACL, or SACL.

## -inheritance

The <b>IADsSecurityUtility</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IADsSecurityUtility</b> also has these types of members:

## -remarks

To read the system access-control list (SACL) of a file or directory, the <b>SE_SECURITY_NAME</b> privilege must be enabled for the calling process. For more information about retrieving the SACL for an object, see <a href="/windows/desktop/AD/retrieving-an-objectampaposs-sacl">Retrieving an Object's SACL</a>.

For more information and a code example that shows how to use the <b>IADsSecurityUtility</b> interface to add an ACE to a file, see <a href="/windows/desktop/ADSI/example-code-for-adding-an-ace-to-a-file">Example Code for Adding an ACE to a File</a>.

## -see-also

<a href="/windows/win32/api/iads/ne-iads-ads_pathtype_enum">ADS_PATHTYPE_ENUM</a>



<a href="/windows/win32/api/iads/ne-iads-ads_sd_format_enum">ADS_SD_FORMAT_ENUM</a>



<a href="/windows/desktop/ADSI/example-code-for-adding-an-ace-to-a-file">Example Code for Adding an ACE to a File</a>



<a href="/windows/desktop/api/iads/nn-iads-iadsaccesscontrolentry">IADsAccessControlEntry</a>



<a href="/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor">IADsSecurityDescriptor</a>



<a href="/windows/desktop/api/iads/nn-iads-iadsaccesscontrollist">IAccessControlList</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/windows/desktop/ADSI/security-descriptors-on-files-and-registry-keys">Security Descriptors on Files and Registry Keys</a>



<a href="/windows/desktop/ADSI/security-interfaces">Security Interfaces</a>
