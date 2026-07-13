---
UID: NF:sysinfoapi.GetProductInfo
title: GetProductInfo function (sysinfoapi.h)
description: Retrieves the product type for the operating system on the local computer, and maps the type to the product types supported by the specified operating system.
helpviewer_keywords: ["GetProductInfo","GetProductInfo function","PRODUCT_BUSINESS","PRODUCT_BUSINESS_N","PRODUCT_CLUSTER_SERVER","PRODUCT_CLUSTER_SERVER_V","PRODUCT_CORE","PRODUCT_CORE_COUNTRYSPECIFIC","PRODUCT_CORE_N","PRODUCT_CORE_SINGLELANGUAGE","PRODUCT_DATACENTER_A_SERVER_CORE","PRODUCT_DATACENTER_EVALUATION_SERVER","PRODUCT_DATACENTER_SERVER","PRODUCT_DATACENTER_SERVER_CORE","PRODUCT_DATACENTER_SERVER_CORE_V","PRODUCT_DATACENTER_SERVER_V","PRODUCT_EDUCATION","PRODUCT_EDUCATION_N","PRODUCT_ENTERPRISE","PRODUCT_ENTERPRISE_E","PRODUCT_ENTERPRISE_EVALUATION","PRODUCT_ENTERPRISE_N","PRODUCT_ENTERPRISE_N_EVALUATION","PRODUCT_ENTERPRISE_S","PRODUCT_ENTERPRISE_SERVER","PRODUCT_ENTERPRISE_SERVER_CORE","PRODUCT_ENTERPRISE_SERVER_CORE_V","PRODUCT_ENTERPRISE_SERVER_IA64","PRODUCT_ENTERPRISE_SERVER_V","PRODUCT_ENTERPRISE_S_EVALUATION","PRODUCT_ENTERPRISE_S_N","PRODUCT_ENTERPRISE_S_N_EVALUATION","PRODUCT_ESSENTIALBUSINESS_SERVER_ADDL","PRODUCT_ESSENTIALBUSINESS_SERVER_ADDLSVC","PRODUCT_ESSENTIALBUSINESS_SERVER_MGMT","PRODUCT_ESSENTIALBUSINESS_SERVER_MGMTSVC","PRODUCT_HOME_BASIC","PRODUCT_HOME_BASIC_E","PRODUCT_HOME_BASIC_N","PRODUCT_HOME_PREMIUM","PRODUCT_HOME_PREMIUM_E","PRODUCT_HOME_PREMIUM_N","PRODUCT_HOME_PREMIUM_SERVER","PRODUCT_HOME_SERVER","PRODUCT_HYPERV","PRODUCT_IOTUAP","PRODUCT_IOTUAPCOMMERCIAL","PRODUCT_MEDIUMBUSINESS_SERVER_MANAGEMENT","PRODUCT_MEDIUMBUSINESS_SERVER_MESSAGING","PRODUCT_MEDIUMBUSINESS_SERVER_SECURITY","PRODUCT_MOBILE_CORE","PRODUCT_MOBILE_ENTERPRISE","PRODUCT_MULTIPOINT_PREMIUM_SERVER","PRODUCT_MULTIPOINT_STANDARD_SERVER","PRODUCT_PROFESSIONAL","PRODUCT_PROFESSIONAL_E","PRODUCT_PROFESSIONAL_N","PRODUCT_PROFESSIONAL_WMC","PRODUCT_PRO_WORKSTATION","PRODUCT_PRO_WORKSTATION_N","PRODUCT_SB_SOLUTION_SERVER","PRODUCT_SB_SOLUTION_SERVER_EM","PRODUCT_SERVER_FOR_SB_SOLUTIONS","PRODUCT_SERVER_FOR_SB_SOLUTIONS_EM","PRODUCT_SERVER_FOR_SMALLBUSINESS","PRODUCT_SERVER_FOR_SMALLBUSINESS_V","PRODUCT_SERVER_FOUNDATION","PRODUCT_SMALLBUSINESS_SERVER","PRODUCT_SMALLBUSINESS_SERVER_PREMIUM","PRODUCT_SMALLBUSINESS_SERVER_PREMIUM_CORE","PRODUCT_SOLUTION_EMBEDDEDSERVER","PRODUCT_STANDARD_A_SERVER_CORE","PRODUCT_STANDARD_EVALUATION_SERVER","PRODUCT_STANDARD_SERVER","PRODUCT_STANDARD_SERVER_CORE","PRODUCT_STANDARD_SERVER_CORE_V","PRODUCT_STANDARD_SERVER_SOLUTIONS","PRODUCT_STANDARD_SERVER_SOLUTIONS_CORE","PRODUCT_STANDARD_SERVER_V","PRODUCT_STARTER","PRODUCT_STARTER_E","PRODUCT_STARTER_N","PRODUCT_STORAGE_ENTERPRISE_SERVER","PRODUCT_STORAGE_ENTERPRISE_SERVER_CORE","PRODUCT_STORAGE_EXPRESS_SERVER","PRODUCT_STORAGE_EXPRESS_SERVER_CORE","PRODUCT_STORAGE_STANDARD_EVALUATION_SERVER","PRODUCT_STORAGE_STANDARD_SERVER","PRODUCT_STORAGE_STANDARD_SERVER_CORE","PRODUCT_STORAGE_WORKGROUP_EVALUATION_SERVER","PRODUCT_STORAGE_WORKGROUP_SERVER","PRODUCT_STORAGE_WORKGROUP_SERVER_CORE","PRODUCT_ULTIMATE","PRODUCT_ULTIMATE_E","PRODUCT_ULTIMATE_N","PRODUCT_UNDEFINED","PRODUCT_WEB_SERVER","PRODUCT_WEB_SERVER_CORE","base.getproductinfo","sysinfoapi/GetProductInfo"]
old-location: base\getproductinfo.htm
tech.root: winprog
ms.assetid: 711e6010-2068-4c97-9009-6ecdf54797b6
ms.date: 12/05/2018
ms.keywords: GetProductInfo, GetProductInfo function, PRODUCT_BUSINESS, PRODUCT_BUSINESS_N, PRODUCT_CLUSTER_SERVER, PRODUCT_CLUSTER_SERVER_V, PRODUCT_CORE, PRODUCT_CORE_COUNTRYSPECIFIC, PRODUCT_CORE_N, PRODUCT_CORE_SINGLELANGUAGE, PRODUCT_DATACENTER_A_SERVER_CORE, PRODUCT_DATACENTER_EVALUATION_SERVER, PRODUCT_DATACENTER_SERVER, PRODUCT_DATACENTER_SERVER_CORE, PRODUCT_DATACENTER_SERVER_CORE_V, PRODUCT_DATACENTER_SERVER_V, PRODUCT_EDUCATION, PRODUCT_EDUCATION_N, PRODUCT_ENTERPRISE, PRODUCT_ENTERPRISE_E, PRODUCT_ENTERPRISE_EVALUATION, PRODUCT_ENTERPRISE_N, PRODUCT_ENTERPRISE_N_EVALUATION, PRODUCT_ENTERPRISE_S, PRODUCT_ENTERPRISE_SERVER, PRODUCT_ENTERPRISE_SERVER_CORE, PRODUCT_ENTERPRISE_SERVER_CORE_V, PRODUCT_ENTERPRISE_SERVER_IA64, PRODUCT_ENTERPRISE_SERVER_V, PRODUCT_ENTERPRISE_S_EVALUATION, PRODUCT_ENTERPRISE_S_N, PRODUCT_ENTERPRISE_S_N_EVALUATION, PRODUCT_ESSENTIALBUSINESS_SERVER_ADDL, PRODUCT_ESSENTIALBUSINESS_SERVER_ADDLSVC, PRODUCT_ESSENTIALBUSINESS_SERVER_MGMT, PRODUCT_ESSENTIALBUSINESS_SERVER_MGMTSVC, PRODUCT_HOME_BASIC, PRODUCT_HOME_BASIC_E, PRODUCT_HOME_BASIC_N, PRODUCT_HOME_PREMIUM, PRODUCT_HOME_PREMIUM_E, PRODUCT_HOME_PREMIUM_N, PRODUCT_HOME_PREMIUM_SERVER, PRODUCT_HOME_SERVER, PRODUCT_HYPERV, PRODUCT_IOTUAP, PRODUCT_IOTUAPCOMMERCIAL, PRODUCT_MEDIUMBUSINESS_SERVER_MANAGEMENT, PRODUCT_MEDIUMBUSINESS_SERVER_MESSAGING, PRODUCT_MEDIUMBUSINESS_SERVER_SECURITY, PRODUCT_MOBILE_CORE, PRODUCT_MOBILE_ENTERPRISE, PRODUCT_MULTIPOINT_PREMIUM_SERVER, PRODUCT_MULTIPOINT_STANDARD_SERVER, PRODUCT_PROFESSIONAL, PRODUCT_PROFESSIONAL_E, PRODUCT_PROFESSIONAL_N, PRODUCT_PROFESSIONAL_WMC, PRODUCT_PRO_WORKSTATION, PRODUCT_PRO_WORKSTATION_N, PRODUCT_SB_SOLUTION_SERVER, PRODUCT_SB_SOLUTION_SERVER_EM, PRODUCT_SERVER_FOR_SB_SOLUTIONS, PRODUCT_SERVER_FOR_SB_SOLUTIONS_EM, PRODUCT_SERVER_FOR_SMALLBUSINESS, PRODUCT_SERVER_FOR_SMALLBUSINESS_V, PRODUCT_SERVER_FOUNDATION, PRODUCT_SMALLBUSINESS_SERVER, PRODUCT_SMALLBUSINESS_SERVER_PREMIUM, PRODUCT_SMALLBUSINESS_SERVER_PREMIUM_CORE, PRODUCT_SOLUTION_EMBEDDEDSERVER, PRODUCT_STANDARD_A_SERVER_CORE, PRODUCT_STANDARD_EVALUATION_SERVER, PRODUCT_STANDARD_SERVER, PRODUCT_STANDARD_SERVER_CORE, PRODUCT_STANDARD_SERVER_CORE_V, PRODUCT_STANDARD_SERVER_SOLUTIONS, PRODUCT_STANDARD_SERVER_SOLUTIONS_CORE, PRODUCT_STANDARD_SERVER_V, PRODUCT_STARTER, PRODUCT_STARTER_E, PRODUCT_STARTER_N, PRODUCT_STORAGE_ENTERPRISE_SERVER, PRODUCT_STORAGE_ENTERPRISE_SERVER_CORE, PRODUCT_STORAGE_EXPRESS_SERVER, PRODUCT_STORAGE_EXPRESS_SERVER_CORE, PRODUCT_STORAGE_STANDARD_EVALUATION_SERVER, PRODUCT_STORAGE_STANDARD_SERVER, PRODUCT_STORAGE_STANDARD_SERVER_CORE, PRODUCT_STORAGE_WORKGROUP_EVALUATION_SERVER, PRODUCT_STORAGE_WORKGROUP_SERVER, PRODUCT_STORAGE_WORKGROUP_SERVER_CORE, PRODUCT_ULTIMATE, PRODUCT_ULTIMATE_E, PRODUCT_ULTIMATE_N, PRODUCT_UNDEFINED, PRODUCT_WEB_SERVER, PRODUCT_WEB_SERVER_CORE, base.getproductinfo, sysinfoapi/GetProductInfo
req.header: sysinfoapi.h
req.include-header: Windows.h
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
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetProductInfo
 - sysinfoapi/GetProductInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-sysinfo-l1-2-7.dll
 - api-ms-win-core-sysinfo-l1-2-6.dll
 - api-ms-win-core-sysinfo-l1-2-5.dll
 - api-ms-win-core-sysinfo-l1-2-4.dll
 - Kernel32.dll
 - API-MS-Win-Core-SysInfo-l1-2-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-SysInfo-l1-2-1.dll
 - API-MS-Win-Core-SysInfo-l1-2-2.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
 - API-MS-Win-Core-SysInfo-l1-2-3.dll
api_name:
 - GetProductInfo
---

# GetProductInfo function


## -description

Retrieves the product type for the operating system on the local computer, and maps the type to the product types supported by the specified operating system.

To retrieve product type information on versions of Windows prior to the minimum supported operating systems specified in the Requirements section, use the <a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getversionexa">GetVersionEx</a> function. You can also use the <b>OperatingSystemSKU</b> property of the <a href="/windows/desktop/CIMWin32Prov/win32-operatingsystem">Win32_OperatingSystem</a> WMI class.

## -parameters

### -param dwOSMajorVersion [in]

The major version number of the operating system. The minimum value is 6.

The combination of the <i>dwOSMajorVersion</i>, <i>dwOSMinorVersion</i>, <i>dwSpMajorVersion</i>, and <i>dwSpMinorVersion</i> parameters describes the maximum target operating system version for the application. For example, Windows Vista and Windows Server 2008 are version 6.0.0.0 and Windows 7 and Windows Server 2008 R2 are version 6.1.0.0. All Windows 10 based releases will be listed as version 6.3.

### -param dwOSMinorVersion [in]

The minor version number of the operating system. The minimum value is 0.

### -param dwSpMajorVersion [in]

The major version number of the operating system service pack. The minimum value is 0.

### -param dwSpMinorVersion [in]

The minor version number of the operating system service pack. The minimum value is 0.

### -param pdwReturnedProductType [out]

The product type. This parameter cannot be <b>NULL</b>. If the specified operating system  is less than the current operating system, this information is mapped to the types supported by the specified operating system. If the specified operating system is greater than the highest supported operating system, this information is mapped to the types supported by the current operating system.


 This parameter can be one of the following values (some products below may be out of support).



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PRODUCT_BUSINESS"></a><a id="product_business"></a><dl>
<dt><b>PRODUCT_BUSINESS</b></dt>
<dt>0x00000006</dt>
</dl>
</td>
<td width="60%">
Business

</td>
</tr>
<tr>
<td width="40%"><a id="PRODUCT_BUSINESS_N"></a><a id="product_business_n"></a><dl>
<dt><b>PRODUCT_BUSINESS_N</b></dt>
<dt>0x00000010</dt>
</dl>
</td>
<td width="60%">
Business N

</td>
</tr>
<tr>
<td width="40%"><a id="PRODUCT_CLUSTER_SERVER"></a><a id="product_cluster_server"></a><dl>
<dt><b>PRODUCT_CLUSTER_SERVER</b></dt>
<dt>0x00000012</dt>
</dl>
</td>
<td width="60%">
HPC Edition

</td>
</tr>
<tr>
<td width="40%"><a id="PRODUCT_CLUSTER_SERVER_V"></a><a id="product_cluster_server_v"></a><dl>
<dt><b>PRODUCT_CLUSTER_SERVER_V</b></dt>
<dt>0x00000040</dt>
</dl>
</td>
<td width="60%">
Server Hyper Core V

</td>
</tr>
<tr>
<td width="40%"><a id="PRODUCT_CORE"></a><a id="product_core"></a><dl>
<dt><b>PRODUCT_CORE</b></dt>
<dt>0x00000065</dt>
</dl>
</td>
<td width="60%">
Windows 10 Home

</td>
</tr>
<tr>
<td width="40%"><a id="PRODUCT_CORE_COUNTRYSPECIFIC"></a><a id="product_core_countryspecific"></a><dl>
<dt><b>PRODUCT_CORE_COUNTRYSPECIFIC</b></dt>
<dt>0x00000063</dt>
</dl>
</td>
<td width="60%">
Windows 10 Home China

</td>
</tr>
<tr>
<td width="40%"><a id="PRODUCT_CORE_N"></a><a id="product_core_n"></a><dl>
<dt><b>PRODUCT_CORE_N</b></dt>
<dt>0x00000062</dt>
</dl>
</td>
<td width="60%">
Windows 10 Home N

</td>
</tr>
<tr>
<td width="40%"><a id="PRODUCT_CORE_SINGLELANGUAGE"></a><a id="product_core_singlelanguage"></a><dl>
<dt><b>PRODUCT_CORE_SINGLELANGUAGE</b></dt>
<dt>0x00000064</dt>
</dl>
</td>
<td width="60%">
Windows 10 Home Single Language

</td>
</tr>
<tr>
<td width="40%"><a id="PRODUCT_DATACENTER_EVALUATION_SERVER"></a><a id="product_datacenter_evaluation_server"></a><dl>
<dt><b>PRODUCT_DATACENTER_EVALUATION_SERVER</b></dt>
<dt>0x00000050</dt>
</dl>
</td>
<td width="60%">
Server Datacenter (evaluation installation)

</td>
</tr>
<tr>
<td width="40%"><a id="PRODUCT_DATACENTER_A_SERVER_CORE"></a><a id="product_datacenter_a_server_core"></a><dl>
<dt><b>PRODUCT_DATACENTER_A_SERVER_CORE</b></dt>
<dt>0x00000091</dt>
</dl>
</td>
<td width="60%">
Server Datacenter, Semi-Annual Channel (core installation)

</td>
</tr>
<tr>
<td width="40%"><a id="PRODUCT_STANDARD_A_SERVER_CORE"></a><a id="product_standard_a_server_core"></a><dl>
<dt><b>PRODUCT_STANDARD_A_SERVER_CORE</b></dt>
<dt>0x00000092</dt>
</dl>
</td>
<td width="60%">
Server Standard, Semi-Annual Channel (core installation)

</td>
</tr>
<tr>
<td width="40%"><a id="PRODUCT_DATACENTER_SERVER"></a><a id="product_datacenter_server"></a><dl>
<dt><b>PRODUCT_DATACENTER_SERVER</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
Server Datacenter (full installation. For Server Core installations of Windows Server 2012 and later, use the method, <a href="/previous-versions/windows/desktop/legacy/hh846315(v=vs.85)">Determining whether Server Core is running</a>.)

</td>
</tr>
<tr>
<td width="40%"><a id="PRODUCT_DATACENTER_SERVER_CORE"></a><a id="product_datacenter_server_core"></a><dl>
<dt><b>PRODUCT_DATACENTER_SERVER_CORE</b></dt>
<dt>0x0000000C</dt>
</dl>
</td>
<td width="60%">
Server Datacenter (core installation, Windows Server 2008 R2 and earlier)

</td>
</tr>
<tr>
<td width="40%"><a id="PRODUCT_DATACENTER_SERVER_CORE_V"></a><a id="product_datacenter_server_core_v"></a><dl>
<dt><b>PRODUCT_DATACENTER_SERVER_CORE_V</b></dt>
<dt>0x00000027</dt>
</dl>
</td>
<td width="60%">
Server Datacenter without Hyper-V (core installation)

</td>
</tr>
<tr>
<td width="40%"><a id="PRODUCT_DATACENTER_SERVER_V"></a><a id="product_datacenter_server_v"></a><dl>
<dt><b>PRODUCT_DATACENTER_SERVER_V</b></dt>
<dt>0x00000025</dt>
</dl>
</td>
<td width="60%">
Server Datacenter without Hyper-V (full installation)

</td>
</tr>
<tr>
<td width="40%"><a id="PRODUCT_EDUCATION"></a><a id="product_education"></a><dl>
<dt><b>PRODUCT_EDUCATION</b></dt>
<dt>0x00000079</dt>
</dl>
</td>
<td width="60%">
Windows 10 Education

</td>
</tr>
<tr>
<td width="40%"><a id="PRODUCT_EDUCATION_N"></a><a id="product_education_n"></a><dl>
<dt><b>PRODUCT_EDUCATION_N</b></dt>
<dt>0x0000007A</dt>
</dl>
</td>
<td width="60%">
Windows 10 Education N

</td>
</tr>
<tr>
<td width="40%"><a id="PRODUCT_ENTERPRISE"></a><a id="product_enterprise"></a><dl>
<dt><b>PRODUCT_ENTERPRISE</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
Windows 10 Enterprise

</td>
</tr>
<tr>
<td width="40%"><a id="PRODUCT_ENTERPRISE_E"></a><a id="product_enterprise_e"></a><dl>
<dt><b>PRODUCT_ENTERPRISE_E</b></dt>
<dt>0x00000046</dt>
</dl>
</td>
<td width="60%">
Windows 10 Enterprise E

</td>
</tr>
<tr>
<td width="40%"><a id="PRODUCT_ENTERPRISE_EVALUATION"></a><a id="product_enterprise_evaluation"></a><dl>
<dt><b>PRODUCT_ENTERPRISE_EVALUATION</b></dt>
<dt>0x00000048</dt>
</dl>
</td>
<td width="60%">
Windows 10 Enterprise Evaluation

</td>
</tr>
<tr>
<td width="40%"><a id="PRODUCT_ENTERPRISE_N"></a><a id="product_enterprise_n"></a><dl>
<dt><b>PRODUCT_ENTERPRISE_N</b></dt>
<dt>0x0000001B</dt>
</dl>
</td>
<td width="60%">
Windows 10 Enterprise N

</td>
</tr>
<tr>
<td width="40%"><a id="PRODUCT_ENTERPRISE_N_EVALUATION"></a><a id="product_enterprise_n_evaluation"></a><dl>
<dt><b>PRODUCT_ENTERPRISE_N_EVALUATION</b></dt>
<dt>0x00000054</dt>
</dl>
</td>
<td width="60%">
Windows 10 Enterprise N Evaluation

</td>
</tr>
<tr>
<td width="40%"><a id="PRODUCT_ENTERPRISE_S"></a><a id="product_enterprise_s"></a><dl>
<dt><b>PRODUCT_ENTERPRISE_S</b></dt>
<dt>0x0000007D</dt>
</dl>
</td>
<td width="60%">
Windows 10 Enterprise 2015 LTSB

</td>
</tr>
<tr>
<td width="40%"><a id="PRODUCT_ENTERPRISE_S_EVALUATION"></a><a id="product_enterprise_s_evaluation"></a><dl>
<dt><b>PRODUCT_ENTERPRISE_S_EVALUATION</b></dt>
<dt>0x00000081</dt>
</dl>
</td>
<td width="60%">
Windows 10 Enterprise 2015 LTSB Evaluation

</td>
</tr>
<tr>
<td width="40%"><a id="PRODUCT_ENTERPRISE_S_N"></a><a id="product_enterprise_s_n"></a><dl>
<dt><b>PRODUCT_ENTERPRISE_S_N</b></dt>
<dt>0x0000007E</dt>
</dl>
</td>
<td width="60%">
Windows 10 Enterprise 2015 LTSB N

</td>
</tr>
<tr>
<td width="40%"><a id="PRODUCT_ENTERPRISE_S_N_EVALUATION"></a><a id="product_enterprise_s_n_evaluation"></a><dl>
<dt><b>PRODUCT_ENTERPRISE_S_N_EVALUATION</b></dt>
<dt>0x00000082</dt>
</dl>
</td>
<td width="60%">
Windows 10 Enterprise 2015 LTSB N Evaluation

</td>
</tr>
<tr>
<td width="40%"><a id="PRODUCT_ENTERPRISE_SERVER"></a><a id="product_enterprise_server"></a><dl>
<dt><b>PRODUCT_ENTERPRISE_SERVER</b></dt>
<dt>0x0000000A</dt>
</dl>
</td>
<td width="60%">
Server Enterprise (full installation)

</td>
</tr>
<tr>
<td width="40%"><a id="PRODUCT_ENTERPRISE_SERVER_CORE"></a><a id="product_enterprise_server_core"></a><dl>
<dt><b>PRODUCT_ENTERPRISE_SERVER_CORE</b></dt>
<dt>0x0000000E</dt>
</dl>
</td>
<td width="60%">
Server Enterprise (core installation)

</td>
</tr>
<tr>
<td width="40%"><a id="PRODUCT_ENTERPRISE_SERVER_CORE_V"></a><a id="product_enterprise_server_core_v"></a><dl>
<dt><b>PRODUCT_ENTERPRISE_SERVER_CORE_V</b></dt>
<dt>0x00000029</dt>
</dl>
</td>
<td width="60%">
Server Enterprise without Hyper-V (core installation) 

</td>
</tr>
<tr>
<td width="40%"><a id="PRODUCT_ENTERPRISE_SERVER_IA64"></a><a id="product_enterprise_server_ia64"></a><dl>
<dt><b>PRODUCT_ENTERPRISE_SERVER_IA64</b></dt>
<dt>0x0000000F</dt>
</dl>
</td>
<td width="60%">
Server Enterprise for Itanium-based Systems

</td>
</tr>
<tr>
<td width="40%"><a id="PRODUCT_ENTERPRISE_SERVER_V"></a><a id="product_enterprise_server_v"></a><dl>
<dt><b>PRODUCT_ENTERPRISE_SERVER_V</b></dt>
<dt>0x00000026</dt>
</dl>
</td>
<td width="60%">
Server Enterprise without Hyper-V (full installation)

</td>
</tr>
<tr>
<td width="40%"><a id="PRODUCT_ESSENTIALBUSINESS_SERVER_ADDL"></a><a id="product_essentialbusiness_server_addl"></a><dl>
<dt><b>PRODUCT_ESSENTIALBUSINESS_SERVER_ADDL</b></dt>
<dt>0x0000003C</dt>
</dl>
</td>
<td width="60%">
Windows Essential Server Solution Additional

</td>
</tr>
<tr>
<td width="40%"><a id="PRODUCT_ESSENTIALBUSINESS_SERVER_ADDLSVC"></a><a id="product_essentialbusiness_server_addlsvc"></a><dl>
<dt><b>PRODUCT_ESSENTIALBUSINESS_SERVER_ADDLSVC</b></dt>
<dt>0x0000003E</dt>
</dl>
</td>
<td width="60%">
Windows Essential Server Solution Additional SVC

</td>
</tr>
<tr>
<td width="40%"><a id="PRODUCT_ESSENTIALBUSINESS_SERVER_MGMT"></a><a id="product_essentialbusiness_server_mgmt"></a><dl>
<dt><b>PRODUCT_ESSENTIALBUSINESS_SERVER_MGMT</b></dt>
<dt>0x0000003B</dt>
</dl>
</td>
<td width="60%">
Windows Essential Server Solution Management

</td>
</tr>
<tr>
<td width="40%"><a id="PRODUCT_ESSENTIALBUSINESS_SERVER_MGMTSVC"></a><a id="product_essentialbusiness_server_mgmtsvc"></a><dl>
<dt><b>PRODUCT_ESSENTIALBUSINESS_SERVER_MGMTSVC</b></dt>
<dt>0x0000003D</dt>
</dl>
</td>
<td width="60%">
Windows Essential Server Solution Management SVC

</td>
</tr>
<tr>
<td width="40%"><a id="PRODUCT_HOME_BASIC"></a><a id="product_home_basic"></a><dl>
<dt><b>PRODUCT_HOME_BASIC</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
Home Basic 

</td>
</tr>
<tr>
<td width="40%"><a id="PRODUCT_HOME_BASIC_E"></a><a id="product_home_basic_e"></a><dl>
<dt><b>PRODUCT_HOME_BASIC_E</b></dt>
<dt>0x00000043</dt>
</dl>
</td>
<td width="60%">
Not supported

</td>
</tr>
<tr>
<td width="40%"><a id="PRODUCT_HOME_BASIC_N"></a><a id="product_home_basic_n"></a><dl>
<dt><b>PRODUCT_HOME_BASIC_N</b></dt>
<dt>0x00000005</dt>
</dl>
</td>
<td width="60%">
Home Basic N

</td>
</tr>
<tr>
<td width="40%"><a id="PRODUCT_HOME_PREMIUM"></a><a id="product_home_premium"></a><dl>
<dt><b>PRODUCT_HOME_PREMIUM</b></dt>
<dt>0x00000003</dt>
</dl>
</td>
<td width="60%">
Home Premium

</td>
</tr>
<tr>
<td width="40%"><a id="PRODUCT_HOME_PREMIUM_E"></a><a id="product_home_premium_e"></a><dl>
<dt><b>PRODUCT_HOME_PREMIUM_E</b></dt>
<dt>0x00000044</dt>
</dl>
</td>
<td width="60%">
Not supported

</td>
</tr>
<tr>
<td width="40%"><a id="PRODUCT_HOME_PREMIUM_N"></a><a id="product_home_premium_n"></a><dl>
<dt><b>PRODUCT_HOME_PREMIUM_N</b></dt>
<dt>0x0000001A</dt>
</dl>
</td>
<td width="60%">
Home Premium N

</td>
</tr>
<tr>
<td width="40%"><a id="PRODUCT_HOME_PREMIUM_SERVER"></a><a id="product_home_premium_server"></a><dl>
<dt><b>PRODUCT_HOME_PREMIUM_SERVER</b></dt>
<dt>0x00000022</dt>
</dl>
</td>
<td width="60%">
Windows Home Server 2011

</td>
</tr>
<tr>
<td width="40%"><a id="PRODUCT_HOME_SERVER"></a><a id="product_home_server"></a><dl>
<dt><b>PRODUCT_HOME_SERVER</b></dt>
<dt>0x00000013</dt>
</dl>
</td>
<td width="60%">
Windows Storage Server 2008 R2 Essentials

</td>
</tr>
<tr>
<td width="40%"><a id="PRODUCT_HYPERV"></a><a id="product_hyperv"></a><dl>
<dt><b>PRODUCT_HYPERV</b></dt>
<dt>0x0000002A</dt>
</dl>
</td>
<td width="60%">
Microsoft Hyper-V Server

</td>
</tr>
<tr>
<td width="40%"><a id="PRODUCT_IOTENTERPRISE"></a><a id="product_iotenterprise"></a><dl>
<dt><b>PRODUCT_IOTENTERPRISE</b></dt>
<dt>0x000000BC</dt>
</dl>
</td>
<td width="60%">
Windows IoT Enterprise
 
</td>
</tr>
<tr>
<td width="40%"><a id="PRODUCT_IOTENTERPRISE_S"></a><a id="product_iotenterprise_s"></a><dl>
<dt><b>PRODUCT_IOTENTERPRISE_S</b></dt>
<dt>0x000000BF</dt>
</dl>
</td>
<td width="60%">
Windows IoT Enterprise LTSC
 
</td>
</tr>
<tr>
<td width="40%"><a id="PRODUCT_IOTUAP"></a><a id="product_iotuap"></a><dl>
<dt><b>PRODUCT_IOTUAP</b></dt>
<dt>0x0000007B</dt>
</dl>
</td>
<td width="60%">
Windows 10 IoT Core

</td>
</tr>
<tr>
<td width="40%"><a id="PRODUCT_IOTUAPCOMMERCIAL"></a><a id="product_iotuapcommercial"></a><dl>
<dt><b>PRODUCT_IOTUAPCOMMERCIAL</b></dt>
<dt>0x00000083</dt>
</dl>
</td>
<td width="60%">
Windows 10 IoT Core Commercial

</td>
</tr>
<tr>
<td width="40%"><a id="PRODUCT_MEDIUMBUSINESS_SERVER_MANAGEMENT"></a><a id="product_mediumbusiness_server_management"></a><dl>
<dt><b>PRODUCT_MEDIUMBUSINESS_SERVER_MANAGEMENT</b></dt>
<dt>0x0000001E</dt>
</dl>
</td>
<td width="60%">
Windows Essential Business Server Management Server

</td>
</tr>
<tr>
<td width="40%"><a id="PRODUCT_MEDIUMBUSINESS_SERVER_MESSAGING"></a><a id="product_mediumbusiness_server_messaging"></a><dl>
<dt><b>PRODUCT_MEDIUMBUSINESS_SERVER_MESSAGING</b></dt>
<dt>0x00000020</dt>
</dl>
</td>
<td width="60%">
Windows Essential Business Server Messaging Server

</td>
</tr>
<tr>
<td width="40%"><a id="PRODUCT_MEDIUMBUSINESS_SERVER_SECURITY"></a><a id="product_mediumbusiness_server_security"></a><dl>
<dt><b>PRODUCT_MEDIUMBUSINESS_SERVER_SECURITY</b></dt>
<dt>0x0000001F</dt>
</dl>
</td>
<td width="60%">
 Windows Essential Business Server Security Server

</td>
</tr>
<tr>
<td width="40%"><a id="PRODUCT_MOBILE_CORE"></a><a id="product_mobile_core"></a><dl>
<dt><b>PRODUCT_MOBILE_CORE</b></dt>
<dt>0x00000068</dt>
</dl>
</td>
<td width="60%">
Windows 10 Mobile

</td>
</tr>
<tr>
<td width="40%"><a id="PRODUCT_MOBILE_ENTERPRISE"></a><a id="product_mobile_enterprise"></a><dl>
<dt><b>PRODUCT_MOBILE_ENTERPRISE</b></dt>
<dt>0x00000085</dt>
</dl>
</td>
<td width="60%">
Windows 10 Mobile Enterprise

</td>
</tr>
<tr>
<td width="40%"><a id="PRODUCT_MULTIPOINT_PREMIUM_SERVER"></a><a id="product_multipoint_premium_server"></a><dl>
<dt><b>PRODUCT_MULTIPOINT_PREMIUM_SERVER</b></dt>
<dt>0x0000004D</dt>
</dl>
</td>
<td width="60%">
Windows MultiPoint Server Premium (full installation)

</td>
</tr>
<tr>
<td width="40%"><a id="PRODUCT_MULTIPOINT_STANDARD_SERVER"></a><a id="product_multipoint_standard_server"></a><dl>
<dt><b>PRODUCT_MULTIPOINT_STANDARD_SERVER</b></dt>
<dt>0x0000004C</dt>
</dl>
</td>
<td width="60%">
Windows MultiPoint Server Standard (full installation)

</td>
</tr>
<tr>
<td width="40%"><a id="PRODUCT_PPI_PRO"></a><a id="product_ppi_pro"></a><dl>
<dt><b>PRODUCT_PPI_PRO</b></dt>
<dt>0x00000077</dt>
</dl>
</td>
<td width="60%">
Windows 10 Team

</td>
</tr>
<tr>
<td width="40%"><a id="PRODUCT_PRO_FOR_EDUCATION"></a><a id="product_pro_for_education"></a><dl>
<dt><b>PRODUCT_PRO_FOR_EDUCATION</b></dt>
<dt>0x000000A4</dt>
</dl>
</td>
<td width="60%">
Windows 10 Pro Education

</td>
</tr>
<tr>
<td width="40%"><a id="PRODUCT_PRO_WORKSTATION"></a><a id="product_pro_workstation"></a><dl>
<dt><b>PRODUCT_PRO_WORKSTATION</b></dt>
<dt>0x000000A1</dt>
</dl>
</td>
<td width="60%">
Windows 10 Pro for Workstations

</td>
</tr>
<tr>
<td width="40%"><a id="PRODUCT_PRO_WORKSTATION_N"></a><a id="product_pro_workstation_n"></a><dl>
<dt><b>PRODUCT_PRO_WORKSTATION_N</b></dt>
<dt>0x000000A2</dt>
</dl>
</td>
<td width="60%">
Windows 10 Pro for Workstations N

</td>
</tr>
<tr>
<td width="40%"><a id="PRODUCT_PROFESSIONAL"></a><a id="product_professional"></a><dl>
<dt><b>PRODUCT_PROFESSIONAL</b></dt>
<dt>0x00000030</dt>
</dl>
</td>
<td width="60%">
Windows 10  Pro

</td>
</tr>
<tr>
<td width="40%"><a id="PRODUCT_PROFESSIONAL_E"></a><a id="product_professional_e"></a><dl>
<dt><b>PRODUCT_PROFESSIONAL_E</b></dt>
<dt>0x00000045</dt>
</dl>
</td>
<td width="60%">
 Not supported

</td>
</tr>
<tr>
<td width="40%"><a id="PRODUCT_PROFESSIONAL_N"></a><a id="product_professional_n"></a><dl>
<dt><b>PRODUCT_PROFESSIONAL_N</b></dt>
<dt>0x00000031</dt>
</dl>
</td>
<td width="60%">
 Windows 10 Pro N

</td>
</tr>
<tr>
<td width="40%"><a id="PRODUCT_PROFESSIONAL_WMC"></a><a id="product_professional_wmc"></a><dl>
<dt><b>PRODUCT_PROFESSIONAL_WMC</b></dt>
<dt>0x00000067</dt>
</dl>
</td>
<td width="60%">
Professional with Media Center

</td>
</tr>
<tr>
<td width="40%"><a id="PRODUCT_SB_SOLUTION_SERVER"></a><a id="product_sb_solution_server"></a><dl>
<dt><b>PRODUCT_SB_SOLUTION_SERVER</b></dt>
<dt>0x00000032</dt>
</dl>
</td>
<td width="60%">
Windows Small Business Server 2011 Essentials

</td>
</tr>
<tr>
<td width="40%"><a id="PRODUCT_SB_SOLUTION_SERVER_EM"></a><a id="product_sb_solution_server_em"></a><dl>
<dt><b>PRODUCT_SB_SOLUTION_SERVER_EM</b></dt>
<dt>0x00000036</dt>
</dl>
</td>
<td width="60%">
Server For SB Solutions EM

</td>
</tr>
<tr>
<td width="40%"><a id="PRODUCT_SERVER_FOR_SB_SOLUTIONS"></a><a id="product_server_for_sb_solutions"></a><dl>
<dt><b>PRODUCT_SERVER_FOR_SB_SOLUTIONS</b></dt>
<dt>0x00000033</dt>
</dl>
</td>
<td width="60%">
Server For SB Solutions

</td>
</tr>
<tr>
<td width="40%"><a id="PRODUCT_SERVER_FOR_SB_SOLUTIONS_EM"></a><a id="product_server_for_sb_solutions_em"></a><dl>
<dt><b>PRODUCT_SERVER_FOR_SB_SOLUTIONS_EM</b></dt>
<dt>0x00000037</dt>
</dl>
</td>
<td width="60%">
Server For SB Solutions EM

</td>
</tr>
<tr>
<td width="40%"><a id="PRODUCT_SERVER_FOR_SMALLBUSINESS"></a><a id="product_server_for_smallbusiness"></a><dl>
<dt><b>PRODUCT_SERVER_FOR_SMALLBUSINESS</b></dt>
<dt>0x00000018</dt>
</dl>
</td>
<td width="60%">
Windows Server 2008 for Windows Essential Server Solutions

</td>
</tr>
<tr>
<td width="40%"><a id="PRODUCT_SERVER_FOR_SMALLBUSINESS_V"></a><a id="product_server_for_smallbusiness_v"></a><dl>
<dt><b>PRODUCT_SERVER_FOR_SMALLBUSINESS_V</b></dt>
<dt>0x00000023</dt>
</dl>
</td>
<td width="60%">
Windows Server 2008 without Hyper-V for Windows Essential Server Solutions

</td>
</tr>
<tr>
<td width="40%"><a id="PRODUCT_SERVER_FOUNDATION"></a><a id="product_server_foundation"></a><dl>
<dt><b>PRODUCT_SERVER_FOUNDATION</b></dt>
<dt>0x00000021</dt>
</dl>
</td>
<td width="60%">
Server Foundation

</td>
</tr>
<tr>
<td width="40%"><a id="PRODUCT_SERVERRDSH"></a><a id="product_serverrdsh"></a><dl>
<dt><b>PRODUCT_SERVERRDSH</b></dt>
<dt>0x000000AF</dt>
</dl>
</td>
<td width="60%">
Windows 10 Enterprise for Virtual Desktops

</td>
</tr>
<tr>
<td width="40%"><a id="PRODUCT_SMALLBUSINESS_SERVER"></a><a id="product_smallbusiness_server"></a><dl>
<dt><b>PRODUCT_SMALLBUSINESS_SERVER</b></dt>
<dt>0x00000009</dt>
</dl>
</td>
<td width="60%">
Windows Small Business Server

</td>
</tr>
<tr>
<td width="40%"><a id="PRODUCT_SMALLBUSINESS_SERVER_PREMIUM"></a><a id="product_smallbusiness_server_premium"></a><dl>
<dt><b>PRODUCT_SMALLBUSINESS_SERVER_PREMIUM</b></dt>
<dt>0x00000019</dt>
</dl>
</td>
<td width="60%">
Small Business Server Premium

</td>
</tr>
<tr>
<td width="40%"><a id="PRODUCT_SMALLBUSINESS_SERVER_PREMIUM_CORE"></a><a id="product_smallbusiness_server_premium_core"></a><dl>
<dt><b>PRODUCT_SMALLBUSINESS_SERVER_PREMIUM_CORE</b></dt>
<dt>0x0000003F</dt>
</dl>
</td>
<td width="60%">
Small Business Server Premium (core installation)

</td>
</tr>
<tr>
<td width="40%"><a id="PRODUCT_SOLUTION_EMBEDDEDSERVER"></a><a id="product_solution_embeddedserver"></a><dl>
<dt><b>PRODUCT_SOLUTION_EMBEDDEDSERVER</b></dt>
<dt>0x00000038</dt>
</dl>
</td>
<td width="60%">
Windows MultiPoint Server

</td>
</tr>
<tr>
<td width="40%"><a id="PRODUCT_STANDARD_EVALUATION_SERVER"></a><a id="product_standard_evaluation_server"></a><dl>
<dt><b>PRODUCT_STANDARD_EVALUATION_SERVER</b></dt>
<dt>0x0000004F</dt>
</dl>
</td>
<td width="60%">
Server Standard (evaluation installation)

</td>
</tr>
<tr>
<td width="40%"><a id="PRODUCT_STANDARD_SERVER"></a><a id="product_standard_server"></a><dl>
<dt><b>PRODUCT_STANDARD_SERVER</b></dt>
<dt>0x00000007</dt>
</dl>
</td>
<td width="60%">
Server Standard (full installation. For Server Core installations of Windows Server 2012 and later, use the method, <a href="/previous-versions/windows/desktop/legacy/hh846315(v=vs.85)">Determining whether Server Core is running</a>.)

</td>
</tr>
<tr>
<td width="40%"><a id="PRODUCT_STANDARD_SERVER_CORE_"></a><a id="product_standard_server_core_"></a><dl>
<dt><b>PRODUCT_STANDARD_SERVER_CORE </b></dt>
<dt>0x0000000D</dt>
</dl>
</td>
<td width="60%">
Server Standard (core installation, Windows Server 2008 R2 and earlier)

</td>
</tr>
<tr>
<td width="40%"><a id="PRODUCT_STANDARD_SERVER_CORE_V"></a><a id="product_standard_server_core_v"></a><dl>
<dt><b>PRODUCT_STANDARD_SERVER_CORE_V</b></dt>
<dt>0x00000028</dt>
</dl>
</td>
<td width="60%">
Server Standard without Hyper-V (core installation)

</td>
</tr>
<tr>
<td width="40%"><a id="PRODUCT_STANDARD_SERVER_V"></a><a id="product_standard_server_v"></a><dl>
<dt><b>PRODUCT_STANDARD_SERVER_V</b></dt>
<dt>0x00000024</dt>
</dl>
</td>
<td width="60%">
Server Standard without Hyper-V

</td>
</tr>
<tr>
<td width="40%"><a id="PRODUCT_STANDARD_SERVER_SOLUTIONS"></a><a id="product_standard_server_solutions"></a><dl>
<dt><b>PRODUCT_STANDARD_SERVER_SOLUTIONS</b></dt>
<dt>0x00000034</dt>
</dl>
</td>
<td width="60%">
Server Solutions Premium 

</td>
</tr>
<tr>
<td width="40%"><a id="PRODUCT_STANDARD_SERVER_SOLUTIONS_CORE"></a><a id="product_standard_server_solutions_core"></a><dl>
<dt><b>PRODUCT_STANDARD_SERVER_SOLUTIONS_CORE</b></dt>
<dt>0x00000035</dt>
</dl>
</td>
<td width="60%">
Server Solutions Premium (core installation)

</td>
</tr>
<tr>
<td width="40%"><a id="PRODUCT_STARTER"></a><a id="product_starter"></a><dl>
<dt><b>PRODUCT_STARTER</b></dt>
<dt>0x0000000B</dt>
</dl>
</td>
<td width="60%">
Starter

</td>
</tr>
<tr>
<td width="40%"><a id="PRODUCT_STARTER_E"></a><a id="product_starter_e"></a><dl>
<dt><b>PRODUCT_STARTER_E</b></dt>
<dt>0x00000042</dt>
</dl>
</td>
<td width="60%">
Not supported

</td>
</tr>
<tr>
<td width="40%"><a id="PRODUCT_STARTER_N"></a><a id="product_starter_n"></a><dl>
<dt><b>PRODUCT_STARTER_N</b></dt>
<dt>0x0000002F</dt>
</dl>
</td>
<td width="60%">
Starter N

</td>
</tr>
<tr>
<td width="40%"><a id="PRODUCT_STORAGE_ENTERPRISE_SERVER"></a><a id="product_storage_enterprise_server"></a><dl>
<dt><b>PRODUCT_STORAGE_ENTERPRISE_SERVER</b></dt>
<dt>0x00000017</dt>
</dl>
</td>
<td width="60%">
Storage Server Enterprise

</td>
</tr>
<tr>
<td width="40%"><a id="PRODUCT_STORAGE_ENTERPRISE_SERVER_CORE"></a><a id="product_storage_enterprise_server_core"></a><dl>
<dt><b>PRODUCT_STORAGE_ENTERPRISE_SERVER_CORE</b></dt>
<dt>0x0000002E</dt>
</dl>
</td>
<td width="60%">
Storage Server Enterprise (core installation)

</td>
</tr>
<tr>
<td width="40%"><a id="PRODUCT_STORAGE_EXPRESS_SERVER"></a><a id="product_storage_express_server"></a><dl>
<dt><b>PRODUCT_STORAGE_EXPRESS_SERVER</b></dt>
<dt>0x00000014</dt>
</dl>
</td>
<td width="60%">
Storage Server Express

</td>
</tr>
<tr>
<td width="40%"><a id="PRODUCT_STORAGE_EXPRESS_SERVER_CORE"></a><a id="product_storage_express_server_core"></a><dl>
<dt><b>PRODUCT_STORAGE_EXPRESS_SERVER_CORE</b></dt>
<dt>0x0000002B</dt>
</dl>
</td>
<td width="60%">
Storage Server Express (core installation)

</td>
</tr>
<tr>
<td width="40%"><a id="PRODUCT_STORAGE_STANDARD_EVALUATION_SERVER"></a><a id="product_storage_standard_evaluation_server"></a><dl>
<dt><b>PRODUCT_STORAGE_STANDARD_EVALUATION_SERVER</b></dt>
<dt>0x00000060</dt>
</dl>
</td>
<td width="60%">
Storage Server Standard (evaluation installation)

</td>
</tr>
<tr>
<td width="40%"><a id="PRODUCT_STORAGE_STANDARD_SERVER"></a><a id="product_storage_standard_server"></a><dl>
<dt><b>PRODUCT_STORAGE_STANDARD_SERVER</b></dt>
<dt>0x00000015</dt>
</dl>
</td>
<td width="60%">
Storage Server Standard

</td>
</tr>
<tr>
<td width="40%"><a id="PRODUCT_STORAGE_STANDARD_SERVER_CORE"></a><a id="product_storage_standard_server_core"></a><dl>
<dt><b>PRODUCT_STORAGE_STANDARD_SERVER_CORE</b></dt>
<dt>0x0000002C</dt>
</dl>
</td>
<td width="60%">
Storage Server Standard (core installation)

</td>
</tr>
<tr>
<td width="40%"><a id="PRODUCT_STORAGE_WORKGROUP_EVALUATION_SERVER"></a><a id="product_storage_workgroup_evaluation_server"></a><dl>
<dt><b>PRODUCT_STORAGE_WORKGROUP_EVALUATION_SERVER</b></dt>
<dt>0x0000005F</dt>
</dl>
</td>
<td width="60%">
Storage Server Workgroup (evaluation installation)

</td>
</tr>
<tr>
<td width="40%"><a id="PRODUCT_STORAGE_WORKGROUP_SERVER"></a><a id="product_storage_workgroup_server"></a><dl>
<dt><b>PRODUCT_STORAGE_WORKGROUP_SERVER</b></dt>
<dt>0x00000016</dt>
</dl>
</td>
<td width="60%">
Storage Server Workgroup

</td>
</tr>
<tr>
<td width="40%"><a id="PRODUCT_STORAGE_WORKGROUP_SERVER_CORE"></a><a id="product_storage_workgroup_server_core"></a><dl>
<dt><b>PRODUCT_STORAGE_WORKGROUP_SERVER_CORE</b></dt>
<dt>0x0000002D</dt>
</dl>
</td>
<td width="60%">
Storage Server Workgroup (core installation)

</td>
</tr>
<tr>
<td width="40%"><a id="PRODUCT_ULTIMATE"></a><a id="product_ultimate"></a><dl>
<dt><b>PRODUCT_ULTIMATE</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Ultimate

</td>
</tr>
<tr>
<td width="40%"><a id="PRODUCT_ULTIMATE_E"></a><a id="product_ultimate_e"></a><dl>
<dt><b>PRODUCT_ULTIMATE_E</b></dt>
<dt>0x00000047</dt>
</dl>
</td>
<td width="60%">
Not supported

</td>
</tr>
<tr>
<td width="40%"><a id="PRODUCT_ULTIMATE_N"></a><a id="product_ultimate_n"></a><dl>
<dt><b>PRODUCT_ULTIMATE_N</b></dt>
<dt>0x0000001C</dt>
</dl>
</td>
<td width="60%">
Ultimate N

</td>
</tr>
<tr>
<td width="40%"><a id="PRODUCT_UNDEFINED"></a><a id="product_undefined"></a><dl>
<dt><b>PRODUCT_UNDEFINED</b></dt>
<dt>0x00000000</dt>
</dl>
</td>
<td width="60%">
An unknown product

</td>
</tr>
<tr>
<td width="40%"><a id="PRODUCT_WEB_SERVER"></a><a id="product_web_server"></a><dl>
<dt><b>PRODUCT_WEB_SERVER</b></dt>
<dt>0x00000011</dt>
</dl>
</td>
<td width="60%">
Web Server (full installation)

</td>
</tr>
<tr>
<td width="40%"><a id="PRODUCT_WEB_SERVER_CORE"></a><a id="product_web_server_core"></a><dl>
<dt><b>PRODUCT_WEB_SERVER_CORE</b></dt>
<dt>0x0000001D</dt>
</dl>
</td>
<td width="60%">
Web Server (core installation)

</td>
</tr>
</table>

## -returns

If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. This function fails if one of the input parameters is invalid.

## -remarks

To detect whether a server role or feature is installed, use the  <a href="/windows/desktop/WmiSdk/win32-serverfeature">Server Feature</a> WMI provider.

Subsequent releases of Windows will map the product types it supports to the set of product types supported by each supported previous release of Windows, back to version 6.0.0.0. Therefore, an application that does an equality test for any of these values will continue to work on future releases, even when new product types are added.

PRODUCT_*_SERVER_CORE values are not returned in Windows Server 2012, and later. For  example, the base server edition, Server Datacenter, is used to build the two different installation options: "full server" and "core server". With Windows Server 2012,  <b>GetProductInfo</b> will return PRODUCT_DATACENTER regardless of the option used during product installation. As noted above, for Server Core installations of Windows Server 2012 and later, use the method <a href="/previous-versions/windows/desktop/legacy/hh846315(v=vs.85)">Determining whether Server Core is running</a>.

The following table indicates the product types that were introduced in 6.1.0.0, and what they will map to if <b>GetProductInfo</b> is called with version 6.0.0.0 on a 6.1.0.0 system.

<table>
<tr>
<th>New for 6.1.0.0</th>
<th>Value returned with 6.0.0.0</th>
</tr>
<tr>
<td>PRODUCT_PROFESSIONAL</td>
<td>PRODUCT_BUSINESS</td>
</tr>
<tr>
<td>PRODUCT_PROFESSIONAL_N</td>
<td>PRODUCT_BUSINESS_N</td>
</tr>
<tr>
<td>PRODUCT_STARTER_N</td>
<td>PRODUCT_STARTER</td>
</tr>
</table>
 

To compile an application that uses this function, define _WIN32_WINNT as 0x0600 or later. For more information, see 
<a href="/windows/desktop/WinProg/using-the-windows-headers">Using the Windows Headers</a>.


#### Examples

For an example, see <a href="/windows/desktop/SysInfo/getting-the-system-version">Getting the System Version</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/SysInfo/system-information-functions">System Information Functions</a>
