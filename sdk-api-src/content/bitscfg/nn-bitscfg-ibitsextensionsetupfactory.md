---
UID: NN:bitscfg.IBITSExtensionSetupFactory
title: IBITSExtensionSetupFactory
author: windows-sdk-content
description: Use the IBITSExtensionSetupFactory interface to get a pointer to the IBITSExtensionSetup interface.
old-location: bits\ibitsextensionsetupfactory.htm
old-project: Bits
ms.assetid: 0105d525-c841-4e0e-bd4a-2a1bcdb0dc4a
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: IBITSExtensionSetupFactory, IBITSExtensionSetupFactory interface [BITS], IBITSExtensionSetupFactory interface [BITS],described, _drz_ibitsextensionsetupfactory, bits.ibitsextensionsetupfactory, bitscfg/IBITSExtensionSetupFactory
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: BITS_FILE_PROPERTY_VALUE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	BitsMgr.dll
api_name:
-	IBITSExtensionSetupFactory
product: Windows
targetos: Windows
req.lib: 
req.dll: BitsMgr.dll
req.irql: 
---

# IBITSExtensionSetupFactory interface


## -description


Use the 
<b>IBITSExtensionSetupFactory</b> interface to get a pointer to the 
<a href="https://msdn.microsoft.com/840608ef-9c07-43f7-9cfd-20996a18bb50">IBITSExtensionSetup</a> interface. Only use this interface if you use the 
<b>IBITSExtensionSetup</b> interface in a setup program that also installs the BITS server. Because the IIS cache does not contain the BITS extensions added during setup, the extensions are not available using the <a href="https://msdn.microsoft.com/595b2c7f-584c-4343-a75c-327d8ed4ceb1">ADsGetObject</a> ADSI function. The 
<b>IBITSExtensionSetupFactory</b> interface provides a 
<a href="https://msdn.microsoft.com/ac0bb9d5-3f1f-4c9b-bd7d-905e0451bf70">GetObject</a> method, which accesses the BITS extensions and performs the same binding as the <b>ADsGetObject</b> function.

To get a pointer to the 
<b>IBITSExtensionSetupFactory</b> interface, call the 
<a href="_com_cocreateinstance">CoCreateInstance</a> function as shown in Example Code.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IBITSExtensionSetupFactory</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IBITSExtensionSetupFactory</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/ac0bb9d5-3f1f-4c9b-bd7d-905e0451bf70">GetObject</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to the 
<a href="https://msdn.microsoft.com/840608ef-9c07-43f7-9cfd-20996a18bb50">IBITSExtensionSetup</a> interface.

</td>
</tr>
</table> 


## -remarks



This interface is registered on the server when you install the BITS server extension.

On Windows Server 2003, use the <b>Windows Components Wizard</b> to install the BITS server extension. From  <b>Control Panel</b>, select <b>Add or Remove Programs</b>. Then, select <b>Add/Remove Windows Components</b> to display the <b>Windows Components Wizard</b>. The BITS server extension is a sub-component of Internet Information Services (IIS) which is a sub-component of Web Application Server.


#### Examples

The following example shows how to use the 
<b>IBITSExtensionSetupFactory</b> interface to get a pointer to the 
<a href="https://msdn.microsoft.com/840608ef-9c07-43f7-9cfd-20996a18bb50">IBITSExtensionSetup</a> interface.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>//Set the BITSUploadEnabled IIS configuration setting.
//The pszPath parameter contains the path to the directory service. 
//For example, "IIS://&lt;machine name&gt;/w3svc/1/&lt;virtual directory&gt;".
//The Enable parameter contains true (enable) or false (disable).
HRESULT SetBITSUploadEnabledSetting(LPWSTR pszPath, bool Enable)
{
  HRESULT hr;
  IBITSExtensionSetupFactory* pExtensionSetupFactory = NULL;
  IBITSExtensionSetup* pExtensionSetup = NULL;

  hr = CoCreateInstance(__uuidof(BITSExtensionSetupFactory),
    NULL, CLSCTX_INPROC_SERVER,
    __UUIDOF(IBITSExtensionSetupFactory),
    (void**)&amp;pExtensionSetupFactory);

  if (SUCCEEDED(hr))
  {
    hr = pExtensionSetupFactory-&gt;GetObject(BSTR(pszPath), &amp;pExtensionSetup);
    if (SUCCEEDED(hr))
    {
      if (Enable)
      {
        hr = pExtensionSetup-&gt;EnableBITSUploads();
      }
      else
      {
        hr = pExtensionSetup-&gt;DisableBITSUploads();
      }

      pExtensionSetup-&gt;Release();
    }
    pExtensionSetupFactory-&gt;Release();
  }

  return hr;
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/840608ef-9c07-43f7-9cfd-20996a18bb50">IBITSExtensionSetup</a>
 

 

