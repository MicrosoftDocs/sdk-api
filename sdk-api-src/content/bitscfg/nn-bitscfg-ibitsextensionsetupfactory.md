---
UID: NN:bitscfg.IBITSExtensionSetupFactory
title: IBITSExtensionSetupFactory (bitscfg.h)
description: Use the IBITSExtensionSetupFactory interface to get a pointer to the IBITSExtensionSetup interface.
old-location: bits\ibitsextensionsetupfactory.htm
tech.root: Bits
ms.assetid: 0105d525-c841-4e0e-bd4a-2a1bcdb0dc4a
ms.date: 12/05/2018
ms.keywords: IBITSExtensionSetupFactory, IBITSExtensionSetupFactory interface [BITS], IBITSExtensionSetupFactory interface [BITS],described, _drz_ibitsextensionsetupfactory, bits.ibitsextensionsetupfactory, bitscfg/IBITSExtensionSetupFactory
ms.topic: interface
f1_keywords:
- bitscfg/IBITSExtensionSetupFactory
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- BitsMgr.dll
api_name:
- IBITSExtensionSetupFactory
targetos: Windows
req.typenames: 
req.redist: BITS 1.5 on  Windows XP
ms.custom: 19H1
---

# IBITSExtensionSetupFactory interface


## -description


Use the 
<b>IBITSExtensionSetupFactory</b> interface to get a pointer to the 
<a href="https://docs.microsoft.com/windows/desktop/api/bitscfg/nn-bitscfg-ibitsextensionsetup">IBITSExtensionSetup</a> interface. Only use this interface if you use the 
<b>IBITSExtensionSetup</b> interface in a setup program that also installs the BITS server. Because the IIS cache does not contain the BITS extensions added during setup, the extensions are not available using the <a href="https://docs.microsoft.com/windows/desktop/api/adshlp/nf-adshlp-adsgetobject">ADsGetObject</a> ADSI function. The 
<b>IBITSExtensionSetupFactory</b> interface provides a 
<a href="https://docs.microsoft.com/windows/desktop/api/bitscfg/nf-bitscfg-ibitsextensionsetupfactory-getobject">GetObject</a> method, which accesses the BITS extensions and performs the same binding as the <b>ADsGetObject</b> function.

To get a pointer to the 
<b>IBITSExtensionSetupFactory</b> interface, call the 
<a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a> function as shown in Example Code.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IBITSExtensionSetupFactory</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IBITSExtensionSetupFactory</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IBITSExtensionSetupFactory</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/bitscfg/nf-bitscfg-ibitsextensionsetupfactory-getobject">GetObject</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to the 
<a href="https://docs.microsoft.com/windows/desktop/api/bitscfg/nn-bitscfg-ibitsextensionsetup">IBITSExtensionSetup</a> interface.

</td>
</tr>
</table> 


## -remarks



This interface is registered on the server when you install the BITS server extension.

On Windows Server 2003, use the <b>Windows Components Wizard</b> to install the BITS server extension. From  <b>Control Panel</b>, select <b>Add or Remove Programs</b>. Then, select <b>Add/Remove Windows Components</b> to display the <b>Windows Components Wizard</b>. The BITS server extension is a sub-component of Internet Information Services (IIS) which is a sub-component of Web Application Server.


#### Examples

The following example shows how to use the 
<b>IBITSExtensionSetupFactory</b> interface to get a pointer to the 
<a href="https://docs.microsoft.com/windows/desktop/api/bitscfg/nn-bitscfg-ibitsextensionsetup">IBITSExtensionSetup</a> interface.


```cpp
//Set the BITSUploadEnabled IIS configuration setting.
//The pszPath parameter contains the path to the directory service. 
//For example, "IIS://<machine name>/w3svc/1/<virtual directory>".
//The Enable parameter contains true (enable) or false (disable).
HRESULT SetBITSUploadEnabledSetting(LPWSTR pszPath, bool Enable)
{
  HRESULT hr;
  IBITSExtensionSetupFactory* pExtensionSetupFactory = NULL;
  IBITSExtensionSetup* pExtensionSetup = NULL;

  hr = CoCreateInstance(__uuidof(BITSExtensionSetupFactory),
    NULL, CLSCTX_INPROC_SERVER,
    __UUIDOF(IBITSExtensionSetupFactory),
    (void**)&pExtensionSetupFactory);

  if (SUCCEEDED(hr))
  {
    hr = pExtensionSetupFactory->GetObject(BSTR(pszPath), &pExtensionSetup);
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
    pExtensionSetupFactory->Release();
  }

  return hr;
}
```





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/bitscfg/nn-bitscfg-ibitsextensionsetup">IBITSExtensionSetup</a>
 

 

