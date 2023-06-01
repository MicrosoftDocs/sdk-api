---
UID: NF:wbemcli.IWbemLocator.ConnectServer
title: IWbemLocator::ConnectServer (wbemcli.h)
description: The IWbemLocator::ConnectServer method creates a connection through DCOM to a WMI namespace on the computer specified in the strNetworkResource parameter.
helpviewer_keywords: ["ConnectServer","ConnectServer method [Windows Management Instrumentation]","ConnectServer method [Windows Management Instrumentation]","IWbemLocator interface","ConnectServer method [Windows Management Instrumentation]","WbemAdministrativeLocator object","ConnectServer method [Windows Management Instrumentation]","WbemAuthenticatedLocator object","ConnectServer method [Windows Management Instrumentation]","WbemLocator object","ConnectServer method [Windows Management Instrumentation]","WbemUnauthenticatedLocator object","IWbemLocator interface [Windows Management Instrumentation]","ConnectServer method","IWbemLocator.ConnectServer","IWbemLocator::ConnectServer","WBEM_FLAG_CONNECT_REPOSITORY_ONLY","WBEM_FLAG_CONNECT_USE_MAX_WAIT","WbemAdministrativeLocator object [Windows Management Instrumentation]","ConnectServer method","WbemAuthenticatedLocator object [Windows Management Instrumentation]","ConnectServer method","WbemLocator object [Windows Management Instrumentation]","ConnectServer method","WbemUnauthenticatedLocator object [Windows Management Instrumentation]","ConnectServer method","_hmm_iwbemlocator_connectserver","wbemcli/IWbemLocator::ConnectServer","wmi.iwbemlocator_connectserver"]
old-location: wmi\iwbemlocator_connectserver.htm
tech.root: wmi
ms.assetid: 92222e08-8622-46c3-9465-cd12260a2ca0
ms.date: 12/05/2018
ms.keywords: ConnectServer, ConnectServer method [Windows Management Instrumentation], ConnectServer method [Windows Management Instrumentation],IWbemLocator interface, ConnectServer method [Windows Management Instrumentation],WbemAdministrativeLocator object, ConnectServer method [Windows Management Instrumentation],WbemAuthenticatedLocator object, ConnectServer method [Windows Management Instrumentation],WbemLocator object, ConnectServer method [Windows Management Instrumentation],WbemUnauthenticatedLocator object, IWbemLocator interface [Windows Management Instrumentation],ConnectServer method, IWbemLocator.ConnectServer, IWbemLocator::ConnectServer, WBEM_FLAG_CONNECT_REPOSITORY_ONLY, WBEM_FLAG_CONNECT_USE_MAX_WAIT, WbemAdministrativeLocator object [Windows Management Instrumentation],ConnectServer method, WbemAuthenticatedLocator object [Windows Management Instrumentation],ConnectServer method, WbemLocator object [Windows Management Instrumentation],ConnectServer method, WbemUnauthenticatedLocator object [Windows Management Instrumentation],ConnectServer method, _hmm_iwbemlocator_connectserver, wbemcli/IWbemLocator::ConnectServer, wmi.iwbemlocator_connectserver
req.header: wbemcli.h
req.include-header: Wbemidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wbemcli.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wbemuuid.lib
req.dll: Wbemcore.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWbemLocator::ConnectServer
 - wbemcli/IWbemLocator::ConnectServer
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wbemcore.dll
api_name:
 - IWbemLocator.ConnectServer
 - WbemAuthenticatedLocator.ConnectServer
 - WbemAdministrativeLocator.ConnectServer
 - WbemUnauthenticatedLocator.ConnectServer
 - WbemLocator.ConnectServer
---

# IWbemLocator::ConnectServer


## -description

The 
<b>IWbemLocator::ConnectServer</b> method creates a connection through DCOM to a WMI namespace on the computer specified in the <i>strNetworkResource</i> parameter.


<a href="/windows/desktop/WmiSdk/swbemlocator-connectserver">SWbemLocator.ConnectServer</a> can connect with computers running IPv6 using an IPv6 address in the <i>strNetworkResource</i> parameter. For more information, see <a href="/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi">IPv6 and IPv4 Support in WMI</a>.

## -parameters

### -param strNetworkResource [in]

Pointer to a valid <b>BSTR</b> that contains the object path of the correct WMI namespace. For local access to the default namespace, use a simple object path: "root\default" or "\\.\root\default". For access to the default namespace on a remote computer using COM or Microsoft-compatible networking, include the computer name: "\\myserver\root\default".  For more information, see 
<a href="/windows/desktop/WmiSdk/describing-a-wmi-namespace-object-path">Describing a WMI Namespace Object Path</a>. The computer name also can  be a DNS name or IP  address. Starting with Windows Vista, <a href="/windows/desktop/WmiSdk/swbemlocator-connectserver">SWbemLocator.ConnectServer</a> can connect with computers running IPv6 using an IPv6 address. For more information, see <a href="/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi">IPv6 and IPv4 Support in WMI</a>.

### -param strUser [in]

Pointer to a valid <b>BSTR</b>, which contains the user name you need for a connection. A <b>NULL</b> value indicates the current security context. If the user name is from a domain different from the current domain, the string may contain the domain name and user name  separated by a backslash.

<code>StrUserName = SysAllocString(L"Domain\\UserName");</code>

The <i>strUser</i> parameter cannot be an empty string.
Note that if the domain is specified in <i>strAuthority</i>, then it must not be specified here. Specifying the domain in both parameters results in an invalid parameter error.

You can use the user principal name (UPN) format, which is <i>Username@DomainName</i> to specify the <i>strUser</i>.

### -param strPassword [in]

Pointer to a valid <b>BSTR</b> that contains the password you need for a connection. A <b>NULL</b> value indicates the current security context. A blank string  ""  specifies a valid zero-length password.

### -param strLocale [in]

If <b>NULL</b>, the current locale is used. If not <b>NULL</b>, this parameter must be a valid <b>BSTR</b>, which indicates the correct locale for information retrieval. For Microsoft locale identifiers, the format of the string is "MS_xxx", where xxx is a string in hexadecimal form that indicates the Local Identification (LCID), for example, American English would appear as "MS_409". If an invalid locale is specified, then the method returns <b>WBEM_E_INVALID_PARAMETER</b>.

<b>Windows 7:  </b>If an invalid locale is specified, then the default locale of the server is used unless there is a server-supported locale provided by the user application.

### -param lSecurityFlags [in]

Long value used to pass flag values to 
<b>ConnectServer</b>. A value of zero (0) for this parameter results in the call to 
<b>ConnectServer</b> returning only after connection to the server is established. This could result in your program ceasing to respond indefinitely if the server is broken. The following list lists the other valid values for <i>lSecurityFlags</i>.



#### WBEM_FLAG_CONNECT_REPOSITORY_ONLY (64 (0x40))

Reserved for internal use. Do not use.



#### WBEM_FLAG_CONNECT_USE_MAX_WAIT (128 (0x80))

The 
<b>ConnectServer</b> call  returns in 2 minutes or less. Use this flag to prevent your program from ceasing to respond indefinitely if the server is broken.

### -param strAuthority [in]

This parameter contains the name of the domain of the user to authenticate.

<i>strAuthority</i> can have the following values:

<ul>
<li>
blank

If you leave this parameter blank, NTLM authentication is used and the NTLM domain of the current user is used. If the domain  is specified in <i>strUser</i>, which is the recommended location, then it must not be specified here. Specifying the domain in both parameters results in an invalid parameter error.

</li>
<li>
Kerberos:&lt;<i>principal name</i>&gt;

Kerberos authentication is used and this parameter should contain a Kerberos principal name.

</li>
<li>
NTLMDOMAIN:&lt;<i>domain name</i>&gt;

NT LAN Manager authentication is used and this parameter should contain an NTLM domain name.

</li>
</ul>

### -param pCtx [in]

Typically, this is <b>NULL</b>. Otherwise, this is a pointer to an 
<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemcontext">IWbemContext</a> object required by one or more dynamic class providers. The values in the context object must be specified in the documentation for the providers in question. For more information about this parameter, see 
<a href="/windows/desktop/WmiSdk/making-calls-to-wmi">Making Calls to WMI</a>.

### -param ppNamespace [out]

Receives a pointer to an 
<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices">IWbemServices</a> object bound to the specified namespace. This pointer has a positive reference count. The caller must call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IWbemServices::Release</a> on the pointer when it is no longer required. This pointer is set to point to <b>NULL</b> when there is an error.

## -returns

This method returns an <b>HRESULT</b> that indicates the status of the method call. The following list lists the value contained within an <b>HRESULT</b>.

COM-specific error codes may be returned if network problems cause you to lose the remote connection to WMI.

These error return codes are defined in the Wbemcli.h file in the WMI section of the PSDK \Include directory. For more information see <a href="/windows/desktop/WmiSdk/wmi-error-constants">WMI Error Constants</a>.

## -remarks

Do not specify <i>strUser</i>, <i>strPassword</i>, or <i>strAuthority</i>  when making a connection to a local namespace. For more information, see <a href="/windows/desktop/WmiSdk/connecting-to-wmi-on-a-remote-computer">Connecting to WMI on a Remote Computer</a>.

For more information on how to use <b>ConnectServer</b>, see <a href="/windows/desktop/WmiSdk/creating-a-connection-to-a-wmi-namespace">Creating a Connection to a WMI Namespace</a>. Note that the connection to <a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemlocator">IWbemLocator</a> is one of the connections that you must shut down at the end of your application, as described in <a href="/windows/desktop/WmiSdk/cleaning-up-and-shutting-down-a-wmi-application">Cleaning up and Shutting Down a WMI Application</a>.

## Examples

For multiple samples that use the <b>ConnectServer</b> method, see <a href="/windows/desktop/WmiSdk/wmi-c---application-examples">WMI C++ Application Examples</a>.

The following C++ code sample describes how to use smi2smir.xml to connect to a specified namespace.

```cpp
int _tmain(int argc, _TCHAR* argv[]) 
{ 
    // Initialize COM. ------------------------------------------ 
    HRESULT hres = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED); 
    if (FAILED(hres)) 
    { 
        wcout << "CoInitializeEx() failure:" << hex << (unsigned long)hres; 
        return 0; 
    } 
 
    // Obtain the initial locator to Windows Management 
    // on a particular host computer. 
    IWbemLocator *pLoc = NULL; 
    hres = CoCreateInstance(CLSID_WbemLocator, 0, CLSCTX_INPROC_SERVER,IID_IWbemLocator, (LPVOID *)&pLoc); 
    if (FAILED(hres)) 
    { 
        CoUninitialize(); 
        wcout << "CreateInstance failure:" << hex << (unsigned long)hres; 
        return 0; 
    } 
 
    // Connect to WMI through the IWbemLocator::ConnectServer method 
    // Connect to the local ROOT\CIMV2 namespace 
    // and obtain pointer pSvc to make IWbemServices calls. 
    IWbemServices *pSvc = NULL;
    BSTR namespace = SysAllocString(L"ROOT\\CimV2");
    hres = pLoc->ConnectServer(namespace, NULL, NULL, 0, NULL, 0, 0, &pSvc);
    SysFreeString(namespace);
 
    if (FAILED(hres)) 
    { 
        pLoc->Release(); 
        CoUninitialize(); 
        wcout << "ConnectServer() failure:" << hex << (unsigned long)hres; 
        return 0; 
    } 
    ...
}
```

## -see-also

<a href="/windows/desktop/WmiSdk/connecting-to-wmi-on-a-remote-computer">Connecting to WMI on a Remote Computer</a>



<a href="/windows/desktop/WmiSdk/creating-a-wmi-application-using-c-">Creating a WMI Application Using C++</a>



<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemlocator">IWbemLocator</a>



<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices">IWbemServices</a>



<a href="/windows/win32/api/wbemcli/ne-wbemcli-wbem_connect_options">WBEM_CONNECT_OPTIONS</a>
