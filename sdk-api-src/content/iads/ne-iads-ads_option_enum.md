---
UID: NE:iads.__MIDL___MIDL_itf_ads_0001_0077_0001
title: ADS_OPTION_ENUM (iads.h)
description: Contains values that indicate the options that can be retrieved or set with the IADsObjectOptions.GetOption and IADsObjectOptions.SetOption methods.
helpviewer_keywords: ["ADS_OPTION_ACCUMULATIVE_MODIFICATION","ADS_OPTION_ENUM","ADS_OPTION_ENUM enumeration [ADSI]","ADS_OPTION_MUTUAL_AUTH_STATUS","ADS_OPTION_PAGE_SIZE","ADS_OPTION_PASSWORD_METHOD","ADS_OPTION_PASSWORD_PORTNUMBER","ADS_OPTION_QUOTA","ADS_OPTION_REFERRALS","ADS_OPTION_SECURITY_MASK","ADS_OPTION_SERVERNAME","ADS_OPTION_SKIP_SID_LOOKUP","_ds_ads_option_enum","adsi.ads__option__enum","adsi.ads_option_enum","iads/ADS_OPTION_ACCUMULATIVE_MODIFICATION","iads/ADS_OPTION_ENUM","iads/ADS_OPTION_MUTUAL_AUTH_STATUS","iads/ADS_OPTION_PAGE_SIZE","iads/ADS_OPTION_PASSWORD_METHOD","iads/ADS_OPTION_PASSWORD_PORTNUMBER","iads/ADS_OPTION_QUOTA","iads/ADS_OPTION_REFERRALS","iads/ADS_OPTION_SECURITY_MASK","iads/ADS_OPTION_SERVERNAME","iads/ADS_OPTION_SKIP_SID_LOOKUP"]
old-location: adsi\ads_option_enum.htm
tech.root: adsi
ms.assetid: afb32e03-7e4e-4df9-87c7-db962d62e5f0
ms.date: 12/05/2018
ms.keywords: ADS_OPTION_ACCUMULATIVE_MODIFICATION, ADS_OPTION_ENUM, ADS_OPTION_ENUM enumeration [ADSI], ADS_OPTION_MUTUAL_AUTH_STATUS, ADS_OPTION_PAGE_SIZE, ADS_OPTION_PASSWORD_METHOD, ADS_OPTION_PASSWORD_PORTNUMBER, ADS_OPTION_QUOTA, ADS_OPTION_REFERRALS, ADS_OPTION_SECURITY_MASK, ADS_OPTION_SERVERNAME, ADS_OPTION_SKIP_SID_LOOKUP, _ds_ads_option_enum, adsi.ads__option__enum, adsi.ads_option_enum, iads/ADS_OPTION_ACCUMULATIVE_MODIFICATION, iads/ADS_OPTION_ENUM, iads/ADS_OPTION_MUTUAL_AUTH_STATUS, iads/ADS_OPTION_PAGE_SIZE, iads/ADS_OPTION_PASSWORD_METHOD, iads/ADS_OPTION_PASSWORD_PORTNUMBER, iads/ADS_OPTION_QUOTA, iads/ADS_OPTION_REFERRALS, iads/ADS_OPTION_SECURITY_MASK, iads/ADS_OPTION_SERVERNAME, iads/ADS_OPTION_SKIP_SID_LOOKUP
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: ADS_OPTION_ENUM
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_ads_0001_0077_0001
 - iads/__MIDL___MIDL_itf_ads_0001_0077_0001
 - ADS_OPTION_ENUM
 - iads/ADS_OPTION_ENUM
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Iads.h
api_name:
 - ADS_OPTION_ENUM
---

# ADS_OPTION_ENUM enumeration


## -description

The <b>ADS_OPTION_ENUM</b> enumeration type 
   contains values that indicate the options that can be retrieved or set with the 
   <a href="/windows/desktop/api/iads/nf-iads-iadsobjectoptions-getoption">IADsObjectOptions.GetOption</a> and 
   <a href="/windows/desktop/api/iads/nf-iads-iadsobjectoptions-setoption">IADsObjectOptions.SetOption</a> 
   methods.

## -enum-fields

### -field ADS_OPTION_SERVERNAME:0

Gets a <b>VT_BSTR</b> that contains the host name of the server for the current binding 
      to this object. This option is not supported by the 
      <a href="/windows/desktop/api/iads/nf-iads-iadsobjectoptions-setoption">IADsObjectOptions.SetOption</a> method.

### -field ADS_OPTION_REFERRALS

Gets or sets a <b>VT_I4</b> value that indicates how referral chasing is performed in a 
      query. This option can contain one of  the 
      values defined by the <a href="/windows/win32/api/iads/ne-iads-ads_chase_referrals_enum">ADS_CHASE_REFERRALS_ENUM</a> 
      enumeration.

### -field ADS_OPTION_PAGE_SIZE

Gets or sets a <b>VT_I4</b> value that indicates the page size in a paged search.

### -field ADS_OPTION_SECURITY_MASK

Gets or sets a <b>VT_I4</b> value that controls the security descriptor data that can be 
      read on the object. This option can contain any combination of the values defined in the 
      <a href="/windows/win32/api/iads/ne-iads-ads_security_info_enum">ADS_SECURITY_INFO_ENUM</a> enumeration.

### -field ADS_OPTION_MUTUAL_AUTH_STATUS

Gets a <b>VT_I4</b> value that determines if mutual authentication is performed by the 
      SSPI layer. If the returned option value contains the <b>ISC_RET_MUTUAL_AUTH</b> flag, 
      defined in Sspi.h, then mutual authentication has been performed. If the returned option value does not contain 
      the <b>ISC_RET_MUTUAL_AUTH</b> flag, then mutual authentication has not been performed. For 
      more information about mutual authentication, see <a href="/windows/desktop/SecAuthN/sspi">SSPI</a>. This 
      option is not supported by the 
      <a href="/windows/desktop/api/iads/nf-iads-iadsobjectoptions-setoption">IADsObjectOptions.SetOption</a> method.

### -field ADS_OPTION_QUOTA

Enables the effective quota and used quota of a security principal to be read. This option takes a 
       <b>VT_BSTR</b> value that contains the security principal that the quotas can be read for. 
       If the security principal string is zero length or the  value is a <b>VT_EMPTY</b> value, 
       the security principal is the currently logged on user. This option is only supported by the 
       <a href="/windows/desktop/api/iads/nf-iads-iadsobjectoptions-setoption">IADsObjectOptions.SetOption</a> method.

### -field ADS_OPTION_PASSWORD_PORTNUMBER

Retrieves or sets a <b>VT_I4</b> value that contains the port number that ADSI uses to 
       establish a connection when the password is set or changed. By default, ADSI uses port 636 to establish a 
       connection to set or change the password.

### -field ADS_OPTION_PASSWORD_METHOD

Retrieves or sets a <b>VT_I4</b> value that specifies the password encoding method. 
       This option can contain one of the values defined in the 
       <a href="/windows/win32/api/iads/ne-iads-ads_password_encoding_enum">ADS_PASSWORD_ENCODING_ENUM</a> 
       enumeration.

### -field ADS_OPTION_ACCUMULATIVE_MODIFICATION

Contains  a <b>VT_BOOL</b> value that specifies if attribute value change operations 
         should be accumulated. By default, when an attribute value is modified more than one time, the previous value 
         change operation is overwritten by the more recent operation. If this option is set to 
         <b>VARIANT_TRUE</b>, each attribute value change operation is accumulated in the cache. 
         When the attribute value updates are committed to the server with the 
         <a href="/windows/desktop/api/iads/nf-iads-iads-setinfo">IADs.SetInfo</a> method, each individual accumulated 
         operation is sent to the server.

When this option has been set to <b>VARIANT_TRUE</b>, it cannot be reset to 
         <b>VARIANT_FALSE</b> for the lifetime of the ADSI object. To reset this option, all 
         references to the ADSI object must be released and the object must be bound to again. When the object is bound 
         to again, this option will be set to <b>VARIANT_FALSE</b> by default.

This option only affects attribute values modified with the 
         <a href="/windows/desktop/api/iads/nf-iads-iads-putex">IADs.PutEx</a> and 
         <a href="/windows/desktop/api/iads/nf-iads-iadspropertylist-putpropertyitem">IADsPropertyList.PutPropertyItem</a> 
         methods. This option is ignored by the <a href="/windows/desktop/api/iads/nf-iads-iads-put">IADs.Put</a> method.

### -field ADS_OPTION_SKIP_SID_LOOKUP

If this option is set on the object, no lookups will be performed (either during the retrieval or during 
       modification). This option affects the <a href="/windows/desktop/api/iads/nn-iads-iads">IADs</a> and 
       <a href="/windows/desktop/api/iads/nn-iads-iadspropertylist">IADsPropertyList</a> interfaces. It is also applicable 
       when retrieving the effective quota usage of a particular user.

## -see-also

<a href="/windows/desktop/ADSI/adsi-enumerations">ADSI Enumerations</a>



<a href="/windows/win32/api/iads/ne-iads-ads_password_encoding_enum">ADS_PASSWORD_ENCODING_ENUM</a>



<a href="/windows/win32/api/iads/ne-iads-ads_security_info_enum">ADS_SECURITY_INFO_ENUM</a>



<a href="/windows/desktop/api/iads/nf-iads-iads-put">IADs.Put</a>



<a href="/windows/desktop/api/iads/nf-iads-iads-putex">IADs.PutEx</a>



<a href="/windows/desktop/api/iads/nf-iads-iads-setinfo">IADs.SetInfo</a>



<a href="/windows/desktop/api/iads/nn-iads-iadsobjectoptions">IADsObjectOptions</a>



<a href="/windows/desktop/api/iads/nf-iads-iadsobjectoptions-getoption">IADsObjectOptions.GetOption</a>



<a href="/windows/desktop/api/iads/nf-iads-iadsobjectoptions-setoption">IADsObjectOptions.SetOption</a>



<a href="/windows/desktop/api/iads/nf-iads-iadspropertylist-putpropertyitem">IADsPropertyList.PutPropertyItem</a>
