---
UID: NN:bitscfg.IBITSExtensionSetup
title: IBITSExtensionSetup (bitscfg.h)
description: Use the IBITSExtensionSetup interface to enable or disable BITS uploads to a virtual directory.
helpviewer_keywords: ["IBITSExtensionSetup","IBITSExtensionSetup interface [BITS]","IBITSExtensionSetup interface [BITS]","described","_drz_ibitsextensionsetup","bits.ibitsextensionsetup","bitscfg/IBITSExtensionSetup"]
old-location: bits\ibitsextensionsetup.htm
tech.root: Bits
ms.assetid: 840608ef-9c07-43f7-9cfd-20996a18bb50
ms.date: 12/05/2018
ms.keywords: IBITSExtensionSetup, IBITSExtensionSetup interface [BITS], IBITSExtensionSetup interface [BITS],described, _drz_ibitsextensionsetup, bits.ibitsextensionsetup, bitscfg/IBITSExtensionSetup
req.header: bitscfg.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2003
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bitscfg.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: BitsMgr.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: BITS 1.5 on Windows XP
ms.custom: 19H1
f1_keywords:
 - IBITSExtensionSetup
 - bitscfg/IBITSExtensionSetup
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - BitsMgr.dll
api_name:
 - IBITSExtensionSetup
---

# IBITSExtensionSetup interface


## -description

Use the 
<b>IBITSExtensionSetup</b> interface to enable or disable BITS uploads to a virtual directory.

This interface is an ADSI extension. To get a pointer to this interface, call the 
<a href="/windows/desktop/api/adshlp/nf-adshlp-adsgetobject">ADsGetObject</a> ADSI function as shown in Example Code.

If you use this interface from a setup program that also installs the BITS server, you must call the 
<a href="/windows/desktop/api/bitscfg/nf-bitscfg-ibitsextensionsetupfactory-getobject">IBITSExtensionSetupFactory::GetObject</a> method to get a pointer to this interface instead of calling the <a href="/windows/desktop/api/adshlp/nf-adshlp-adsgetobject">ADsGetObject</a> function.

## -inheritance

The <b>IBITSExtensionSetup</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IBITSExtensionSetup</b> also has these types of members:

## -remarks

This interface is registered on the server when you install the BITS server extension.

On Windows Server 2003, use the <b>Windows Components Wizard</b> to install the BITS server extension. From  <b>Control Panel</b>, select <b>Add or Remove Programs</b>. Then, select <b>Add/Remove Windows Components</b> to display the <b>Windows Components Wizard</b>. The BITS server extension is a sub-component of Internet Information Services (IIS) which is a sub-component of Web Application Server.


#### Examples

The following example shows how to use the <b>ADsGetObject</b> function to get a pointer to the 
<b>IBITSExtensionSetup</b> interface.


```cpp
//Set the BITSUploadEnabled IIS configuration setting.
//The pszPath parameter contains the path to the directory service. 
//For example, "IIS://<machine name>/w3svc/1/<virtual directory>".
//The Enable parameter contains true (enable) or false (disable).
HRESULT SetBITSUploadEnabledSetting(LPWSTR pszPath, bool Enable)
{
  HRESULT hr;
  IBITSExtensionSetup* pExtensionSetup = NULL;

  hr = ADsGetObject(pszPath, __uuidof(IBITSExtensionSetup), &pExtensionSetup);
  if (SUCCEEDED(hr))
  {
    if (Enable)
    {
      hr = pExtensionSetup->EnableBITSUploads();
    }
    else
    {
      hr = pExtensionSetup->DisableBITSUploads();
    }

    pExtensionSetup->Release();
  }

  return hr;
}
```

## -see-also

<a href="/windows/desktop/api/bitscfg/nn-bitscfg-ibitsextensionsetupfactory">IBITSExtensionSetupFactory</a>
