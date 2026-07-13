---
UID: NF:netlistmgr.INetwork2.IsDomainAuthenticatedBy
title: INetwork2::IsDomainAuthenticatedBy
description: Queries whether the specified domain authentication method succeeded for this network.
tech.root: nla
ms.date: 04/07/2022
req.construct-type: function
req.header: netlistmgr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 11 Build 22621
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: netlistmgr.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
f1_keywords:
 - INetwork2::IsDomainAuthenticatedBy
 - netlistmgr/INetwork2::IsDomainAuthenticatedBy
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - netlistmgr.h
api_name:
 - INetwork2::IsDomainAuthenticatedBy
helpviewer_keywords:
 - IsDomainAuthenticatedBy
prerelease: false
---

## -description

Queries whether the specified domain authentication method succeeded for this network.

## -parameters

### -param domainAuthenticationKind

Type: \[in\] **[NLM_DOMAIN_AUTHENTICATION_KIND](ne-netlistmgr-nlm_domain_authentication_kind.md)**

The specific domain authentication method to query about.

### -param pValue

Type: \[out, retval\] **[BOOL](/windows/win32/winprog/windows-data-types)\***

The function dereferences *pValue*, and assigns `TRUE` if this network has the same domain authentication kind as that specified in the *domainAuthenticationKind* parameter; or `FALSE` if this network has a different domain authentication kind from that specified in *domainAuthenticationKind*.

## -returns

Returns **S_OK** if successful.

## Example

In this example, a hypothetical networking diagnostic tool seeks to ensure that connections to a corporate network have correct authentication properties.

```cpp
void LogToConsole(std::wstring output, std::wstring networkName)
{
	// Implementation not shown for brevity.
}

void RunDiagnostics()
{
	winrt::com_ptr<::INetworkListManager> nlm;
	winrt::com_ptr<::IEnumNetworks> enumNetworks;
	winrt::com_ptr<::INetwork> network;
	ULONG numberOfNetworksEnumerated{ 0 };
	winrt::check_hresult(::CoCreateInstance(CLSID_NetworkListManager, nullptr, CLSCTX_ALL, IID_PPV_ARGS(&nlm)));
	winrt::check_hresult(nlm->GetNetworks(NLM_ENUM_NETWORK_ALL, enumNetworks.put()));

	while ((enumNetworks->Next(1, network.put(), &numberOfNetworksEnumerated) == S_OK))
	{
		try
		{
			if (numberOfNetworksEnumerated == 1)
			{
				winrt::com_ptr<::INetwork2> network2{ network.as<::INetwork2>() };
				BSTR networkName{};
				HRESULT hr{ network2->GetName(&networkName) };
				winrt::check_hresult(network2->GetName(&networkName));

				BOOL isLdapAuthenticated{ FALSE };
				BOOL isTlsAuthenticated{ FALSE };
				BOOL isNotDomainAuthenticated{ FALSE };
				winrt::check_hresult(network2->IsDomainAuthenticatedBy(NLM_DOMAIN_AUTHENTICATION_KIND_LDAP, &isLdapAuthenticated));
				winrt::check_hresult(network2->IsDomainAuthenticatedBy(NLM_DOMAIN_AUTHENTICATION_KIND_TLS, &isTlsAuthenticated));
				winrt::check_hresult(network2->IsDomainAuthenticatedBy(NLM_DOMAIN_AUTHENTICATION_KIND_NONE, &isNotDomainAuthenticated));

				if (!isNotDomainAuthenticated)
				{
					if (!!isLdapAuthenticated)
					{
						LogToConsole(L"Network is domain authenticated via LDAP", networkName);
					}

					if (!!isTlsAuthenticated)
					{
						LogToConsole(L"Network is domain authenticated via TLS", networkName);
					}

					if (!isLdapAuthenticated && !isTlsAuthenticated)
					{
						LogToConsole(L"Network was not expected to be domain authenticated for any other kinds", networkName);
					}
				}
				else
				{
					LogToConsole(L"Network is not domain authenticated", networkName);
				}
			}
		}
		catch (...)
		{
			// Handle exception.
		}
	}
}
```

## -see-also

* [INetworkConnection2::IsDomainAuthenticatedBy method](nf-netlistmgr-inetworkconnection2-isdomainauthenticatedby.md)
